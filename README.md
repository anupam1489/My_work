awk 'BEGIN { i=1; while(i<=10) { print i*99; i=i+1;} exit;}'-----only to do calculation not for any input

ls -l | head | awk '{print NF}' -------------prints number of fields in ls -l

ls -l | head | awk '{print NF,NR}'-----------prints number of fields in ls -l and line number

There are only a few commands in AWK. The list and syntax follows:

    if ( conditional ) statement [ else statement ]
    while ( conditional ) statement
    for ( expression ; conditional ; expression ) statement
    for ( variable in array ) statement
    break
    continue
    { [ statement ] ...}
    variable=expression
    print [ expression-list ] [ > expression ]
    printf format [ , expression-list ] [ > expression ]
    next
    exit


-------------query to get the list of all PFs in OWB------------------------------------
SELECT DISTINCT obj.OBJECT_NAME,
                CASE
                  WHEN pf.OBJECT_NAME IS NULL THEN
                   'PARENT'
                  ELSE
                   'CHILD'
                END AS PRNT_IND
  FROM OWBSYS.ALL_RT_OBJECTS obj,
       (SELECT DISTINCT OBJECT_NAME
          FROM OWBSYS.ALL_RT_TASKS
         WHERE OBJECT_NAME IS NOT NULL
           AND OBJECT_TYPE = 'ProcessFlow'
           AND CONTEXT_OBJECT_NAME <> OBJECT_NAME) pf
 WHERE obj.OBJECT_TYPE = 'ProcessFlow'
   AND obj.OBJECT_NAME = pf.OBJECT_NAME(+)
   
   ------------------LAST QRY-------------------------------------------------
select  (select NAME
          from ximdw.CDP_IT_SERVICE_STG1 b
         where b.IT_SERVICE_ID = M.IT_SERVICE_ID) as "Application Name",
       (select NAME
          from ximdw.cdp_its_component_stg1 c
         where c.ITS_COMPONENT_ID(+) = M.IT_SERVICE_COMPONENT) as "COMPONENT ID",
       count(n.std) as standalone,
       count(RFA) as RFAonly,
       count(RFS) as RFSonly,
       count(BOTH) as BOTHRFSRFA
  from ximdw.cdp_req_incident_stg1 M,
       (select IDD,
               (case
                 when TYP like 'INCD' or TYP is NULL then
                  'S'
               end) STD,
               (case
                 when TYP like '%RFS%' and TYP NOT LIKE '%RFA%' then
                  'RFS'
               end) RFS,
               (case
                 when TYP like '%RFA%' and TYP NOT LIKE '%RFS%' then
                  'RFA'
               end) RFA,
               (case
                 when length(TYP) > 3 and TYP like '%RFA%RFS%' then
                  'BOTH'
               end) BOTH,
               TYP
          from (select request_incident_id IDD,
                       listagg(f.CHILD_TYPE, ',') WITHIN GROUP(ORDER BY f.child_type) as TYP
                  from (select * from ximdm.cdp_relations_f) f,
                       ximdw.cdp_req_incident_stg1 A
                 where A.IT_SERVICE_GROUP_ID = 22
                   and assigned_group = 22
                   and trunc(request_ts, 'MON') = '1-AUG-2014'
                   and PARENT_ID(+) = request_incident_id
                 group by request_incident_id)
         order by TYP) N
 where M.request_incident_id = n.IDD
 group by rollup(IT_SERVICE_ID, IT_service_component)
 
 -------------------------how to supress repeating rows --------------
with rpt as(select c.*
,rownum rn
from (select a.dname
,b.ename
from dept a
inner join emp b
on a.deptno = b.deptno
order by 1,2) c)
select case
when a.dname = b.dname then ' '
else a.dname
end dname
,a.ename
from rpt a left outer join rpt b
on a.rn = b.rn + 1
order by a.rn;
------------steps to get SQL Plan;


select sql_hash_value hash_value, module
from v$session
where sid = 798;

SELECT
t.sql_text
FROM v$sqltext t
WHERE t.hash_value = 2422958808
ORDER BY t.piece

SELECT LPAD(' ', 2 * (LEVEL - 1)) ||
       DECODE(id,
              0,
              operation || ' (Cost = ' || position || ')',
              LEVEL - 1 || '.' || NVL(position, 0) || ' ' || operation || ' ' ||
              options || ' ' || object_name || ' ' || object_node) "Query Plan"
  FROM (select distinct id,
                        parent_id,
                        operation,
                        cost,
                        position,
                        options,
                        object_name,
                        object_node
          FROM v$sql_plan
         where hash_value = 2422958808)
 START WITH id = 0
CONNECT BY PRIOR id = parent_id

------------------
Displays CPU usage for each User. Useful to understand database load by user.
SELECT ss.username, se.SID, VALUE / 100 cpu_usage_seconds
    FROM v$session ss, v$sesstat se, v$statname sn
   WHERE     se.STATISTIC# = sn.STATISTIC#
         AND NAME LIKE '%CPU used by this session%'
         AND se.SID = ss.SID
         AND ss.status = 'ACTIVE'
         AND ss.username IS NOT NULL
ORDER BY VALUE DESC;
Long Query progress in database

Show the progress of long running queries.
SELECT a.sid,
         a.serial#,
         b.username,
         opname OPERATION,
         target OBJECT,
         TRUNC (elapsed_seconds, 5) "ET (s)",
         TO_CHAR (start_time, 'HH24:MI:SS') start_time,
         ROUND ( (sofar / totalwork) * 100, 2) "COMPLETE (%)"
    FROM v$session_longops a, v$session b
   WHERE     a.sid = b.sid
         AND b.username NOT IN ('SYS', 'SYSTEM')
         AND totalwork > 0
ORDER BY elapsed_seconds;
Get current session id, process id, client process id?

This is for those who wants to do some voodoo magic using process ids and session ids.
SELECT b.sid,
       b.serial#,
       a.spid processid,
       b.process clientpid
  FROM v$process a, v$session b
 WHERE a.addr = b.paddr AND b.audsid = USERENV ('sessionid');

    V$SESSION.SID AND V$SESSION.SERIAL# is database process id
    V$PROCESS.SPID is shadow process id on this database server
    V$SESSION.PROCESS is client PROCESS ID, ON windows it IS : separated THE FIRST # IS THE PROCESS ID ON THE client AND 2nd one IS THE THREAD id.

Last SQL Fired from particular Schema or Table:
SELECT CREATED, TIMESTAMP, last_ddl_time
  FROM all_objects
 WHERE     OWNER = 'MYSCHEMA'
       AND OBJECT_TYPE = 'TABLE'
       AND OBJECT_NAME = 'EMPLOYEE_TABLE';
Find Top 10 SQL by reads per execution
SELECT *
  FROM (  SELECT ROWNUM,
                 SUBSTR (a.sql_text, 1, 200) sql_text,
                 TRUNC (
                    a.disk_reads / DECODE (a.executions, 0, 1, a.executions))
                    reads_per_execution,
                 a.buffer_gets,
                 a.disk_reads,
                 a.executions,
                 a.sorts,
                 a.address
            FROM v$sqlarea a
        ORDER BY 3 DESC)
 WHERE ROWNUM < 10;
Oracle SQL query over the view that shows actual Oracle connections.
SELECT osuser,
         username,
         machine,
         program
    FROM v$session
ORDER BY osuser;
Oracle SQL query that show the opened connections group by the program that opens the connection.
SELECT program application, COUNT (program) Numero_Sesiones
    FROM v$session
GROUP BY program
ORDER BY Numero_Sesiones DESC;
Oracle SQL query that shows Oracle users connected and the sessions number for user
SELECT username Usuario_Oracle, COUNT (username) Numero_Sesiones
    FROM v$session
GROUP BY username
ORDER BY Numero_Sesiones DESC;
Get number of objects per owner
SELECT owner, COUNT (owner) number_of_objects
    FROM dba_objects
GROUP BY owner
ORDER BY number_of_objects DESC;

---------------------------------------------------

