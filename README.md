# My_work
oracle/unix
.LOG
DWHP
stg_ext/DWstGK8123

isrvedr/dec#2012

sheleveri pradeep:9060996996 

w3zljprp/P@$sw0rd!



tspmftp/rbc98k43


Uswu50078
Leelamar$16

-------------
dba_role_priv tbale to chk user access
-------------
mpsiadmin/tcsps2012
---823 server login
./arcgismanager
Password@08

ADP-->Defranco, Glen <Glen.Defranco@xerox.com>
-------------users with in this table are able to save reports-----------
WFAPPL.wf_users
  wfappl.wf_usersgroups
q3k4s81m
Feb@2013

isrvedw/ironman#jan2011
application CRPS--------

 usog49897
 Xerox@Cprs

XAP----
http://xww.isrve.world.xerox.com/CTCDashboards/XapController.go



MPSCTC---dblink----NOETIXCONNECT1.WORLD
select * from dba_db_links where upper(host) like '%NAOP%'

----NAGL dblink:APPSDB.APPS.MC.XEROX.COM

NAF_DM	APPSDB.APPS.MC.XEROX.COM	XRX_NAF_RO	NAF_APPSDB	2/13/2009 4:53:03 PM


\\192.168.1.67\---local share
mc0300ux006.apps.mc.xerox.com

XSAT--->USA.Phoenix.Application.Support@xerox.com

xsat-->XSAT_feedbalance.CSV-->feed from source at /u25/ftp/ISRVE_FEEDS_IN/FBAL-----

USA GSA Shared Services RT Support---nagios dl

1 ftp_fbal ftp_group    1078 Oct 23 11:36 XSAT_feedbalance.CSV
to rename the file:ftp_fbal/Xrxfbal123#

BUILD_MGR/intstlr#sep2014@mc0300ux006.apps.mc.xerox.com:1531/ISRVEPROD
I've changed the iSRVE BUILD_MGR account password to power#sep2013

-------
for RDM(Request and Deployment Management) and ALM(Application Lifecycle Management) 
---------------------------
load_datafiles.sh---mps portals script

-----athena credentials--------DWHP
gdeeti
Jul@2014

su_owbdwhp

-----DWHP --VNC---
athena.wvdc.xerox.net:4
----------
NAF access:

select * from NAF_DM.NAF_SECURITY_LT where s3_id = 'UST41131' 
-----------ary with both RFS and RFA tagged----



 select parent_id,count(1)
   from ximdm.cdp_relations_f f,ximdw.cdp_req_incident_stg1 a
  where  parent_type = 'INCD'
  and child_type = 'RFS' 
  AND parent_id in (select parent_id from ximdm.cdp_relations_f b where  b.parent_id = f.parent_id and child_type = 'RFA')
  and a.REQUEST_INCIDENT_ID=f.parent_id
  and a.it_service_group_id = 22
           and a.assigned_group = 22
           and trunc(a.request_ts, 'MON') = trunc(sysdate-30, 'MON')
  group by parent_id

--------------List of business users-------
select * FROM 
	ISRVETOOLS.USERS U where id in (select user_id FROM ISRVETOOLS.business_area_users) 
-------------business owners/areas---------
select * FROM ISRVETOOLS.business_area
------------
select *
  from cdc_usr.cdp_mirrorcnt_ctl
 WHERE project_name like 'PHNX_PROD' and trunc(source_ts)=trunc(sysdate)-------qry to chk phnx load refresh

01HW562303---
2:58 PM 8/29/2013

----------XSC_PF--------------feed
/home/tspmftp/FUSION/FEEDS/XCS/isrve.read.errors


-------xsbi--------
 IL - _http://xsbiil.corp.xerox.com/XSBIIL/
  PA - _http://xsbipa.corp.xerox.com/XSBI

provide logs

XIMDM.CDP_SELECTIONS_LT
----------standard service--------
select * from XIMDW.CDP_IT_STD_SERVICE_STG1 where std_service_id =62442 
-----------------------------------
source
how frequently and 
today it got loaded or not?

669916
ani,esh
  usog89497
  Xeroxsep2013

CDP_REAL_TIME_REFRESH_PF
BPEL-- XOG MPS team

363459
11:13 AM 8/30/2013

US976966-- Guerin, Michael H

select * from ximdw.cdp_sla_stg1 where it_service_id = 27--qry for sla


Please use the below queries to monitor the reports release, Let me know if you have any questions-- select * from ISRVETOOLS.REPORT_DELIVERY

To check when is the last time reports release has triggered and at what time and also whether report release is still in progress(status=1) 
select * from isrvetools.SCHEDULE_RELEASE_STATUS order by release_id desc

to check what are the reports which are ready for release 
select * from isrvetools.SCHEDULE_REPORTS_QUEUE

To check what are the reports which are getting release(status=1) and also the reports which got released already
select * from isrvetools.SCHEDULE_REPORTS_RELEASE_LOG order by release_id desc

To check failed report get release_id from isrvetools.SCHEDULE_REPORTS_RELEASE_LOG table and pass the same below
Select * from isrvetools.botlog_report where run_id =212 and error_code =1

select * from rc_admin.bottask---to chk the type of report released

7:59 PM 8/30/2013

update ISRVEDW.MSS_EXCESS_STG set STATE=trim(STATE) where length(state)>2 ; 
commit; 

need to provide feed files to ellen for 27-aug-2013--pls refer rupas mail..
-------------

XIM FSC -- create RFS and close

wks_Weekly_JELHCLEANUP -
------need to uncomment --

prd_gldfeed_mjagtf

##PA##runowb OWB_RT FUSION_PF_LOC PROCESS M_GLDFEED , V_MM=$EPMON,V_YYYY=$EPYR
##PA##runowb OWB_RT FUSION_PF_LOC PROCESS M_MJAGTF , V_MM=$EPMON,V_YYYY=$EPYR

------------
ORA-20999: Error in rdr_month_activities_prc-20999ORA-20999: Error in rdr_month_flsm_activities_prc-20005ORA-20005: Error analyzing partitnion in table 

RDR_MONTH_ACTIVITIES_SUM_F ORA-01403: no data found
ORA-06512: at "SNMDM.RDR_MONTH_ACTIVITIES_PRC", line 257
ORA-06512: at line 1-


-----------link to imperonate the user in USCO------------
http://13.129.12.67:9120/CTCDashboards/UscoController.go?UID=US976966






-------usco doar ----------
select * from isrvetools.reqparm where upper(created_by)='US976966' and report_id in ('2017','2001')and saved_request_name is not null order by request_id desc

----------

ORA-20999:  Error in ISRVE_UTL.FEED_MANAGEMENT_PKG.FEED_BALANCING_START ORA-20999:  Error in ISRVE_UTL.FEED_MANAGEMENT_PKG.FEED_BALANCING ORA-20999:  Rejection limit 

has crossed the threshold value
ORA-06512: at "ISRVE_UTL.FEED_MANAGEMENT_PKG", line 89
ORA-06512: at line 1

------------


UPDATE_REPORTING_LOAD_DATES -----


select * from dba_external_locations


CCT.DAT

CUSTOMER.DAT

CHANNEL.DAT

CHANRPT.DAT

CUSTINT.DAT




SFTP_FSC_VZN_FILE_CSH 


----------
--------table which contains all schedule details reportcaster--------
select * from rc_admin.botsched 
-------select scheduleid from rc_admin.botparms where scheduleid = 'S17teoi2o9n9'--0 after deletion
select schedule_id from isrvetools.reqparm where schedule_id = 'S17teoi2o9n9'
-------------------------




Mikes USCO Level DOAR




  usco_scr_profile.csv --
  usco_scr_user_security.csv --not present
  XNAC2DTT_SBU.csv --not present
  USCO_SCORECARD_ORG.csv---rw-r--r--+  1 isrveprd staff       3755 Mar 29  2012 USCO_SCORECARD_ORG.csv_Mar29
  GDO_Retention.csv---rwxr-xr--   1 ftp_ussg ftp_group     674 Mar 11 08:42 GDO_Retention.csv_jan
  -rwxr-xr--   1 ftp_ussg ftp_group     674 Mar 11 08:42 GDO_Retention.csv_jan
  usco_finance_data.csv    -rw-r--r--   1 ftp_ussg ftp_group 2328515 Jun 14 14:12 usco_finance_data.csv_15062013_bkp
  USCO_KEY_BUSS_CNTL_ASSMENT.csv
  are these files present in /u25/ftp/ISRVE_FEEDS_IN/USSG/
  ?
  for today's load?
  USCO_SCR_DAILY_PF

-----------
ORA-20006: Error while dropping partition in table CFU_SUMMARY_DATA_F ORA-02149: Specified partition does not exist
ORA-06512: at "ISRVE_UTL.ISRVE_UTL_PKG", line 515
ORA-06512: at line 1

usa7061ux300


usa7061as113

usa7061as116

--------qury to check nagl refresh-----------
select * from naf_dm.naf_debug where trunc(start_time_stamp)>=trunc(sysdate-1)  order by end_time_stamp desc

Server OS/HW Status (Production) 	RFA#/owner	Database Version (Production) 	RFA#/Owner	Application Version (Production) 	RFA#/Owner	

business impact if unavailable

--------------MPS BI LINK-----------
_https://mpsbi.services.xerox.com/MPS_Integration/MpsController.go
  usog90152/Jul@2013
usxu62456/Xerox345 
USWU50078/Mahesh!09
-------------

mv /u25/ftp/ISRVE_FEEDS_IN/GRS/grs_colorant_supply_hist.csv.Z /u25/ftp/ISRVE_FEEDS_ARCHS/GRS/grs_colorant_supply_hist.csv.Z."`date +%Y%m%d:%T`";
mv /u25/ftp/ISRVE_FEEDS_IN/GRS/grs_meter_read_hist.csv.Z /u25/ftp/ISRVE_FEEDS_ARCHS/GRS/grs_meter_read_hist.csv.Z."`date +%Y%m%d:%T`";
mv /u25/ftp/ISRVE_FEEDS_IN/GRS/grs_asr_machine.csv.Z /u25/ftp/ISRVE_FEEDS_ARCHS/GRS/grs_asr_machine.csv.Z."`date +%Y%m%d:%T`";
------------



update USWU47296.ISRVE_JOBS_MAST set ACTIVE_STATUS = 'N',DELAY_STATUS = 'N',COMMENTS = 'retired as part of RFC495737' where process_name = 'MCKB_DAILY_DATA_LOAD_PF';
update USWU47296.ISRVE_JOBS_MAST set ACTIVE_STATUS = 'N',DELAY_STATUS = 'N',COMMENTS = 'retired as part of RFC495737' where process_name = 

'CDSI_RESPONSE_LOAD_DAILY_PF';  

exec sys.update_itt('673615');
----
SLT__desc isrve

select * from XIMDM.CDP_SELECTIONS_LT  where it_service_group_id =22


-------
Robert.Erath@xerox.com

Robert.Erath@xerox.com

------------
usa7061as121---boxi
usa0300vm534---pervasave 

--9985117596


5852658734---laxman gawadi --USA NASPD TCS DBA <USA.NASPD.TCS.DBA@xerox.com>---naop team for MPSCTC

#0001 585 265 8734 #668942
---------------1064 login-
uswu50078
Leelamar+16
Leelamar##16
---------------
Janakiramjul@15
5:22 PM 9/17/2013




ORA-20006: Error while dropping partition in table CFU_SUMMARY_DATA_F ORA-02149: Specified partition does not exist
ORA-06512: at "ISRVE_UTL.ISRVE_UTL_PKG", line 515
ORA-06512: at line 1
------------
ORA-02149: Specified partition does not exist
    Cause: Partition not found for the object.
    Action: Retry with correct partition name





Hintz, Terry E <Terry.Hintz@xerox.com>

Business Objects Enterprise (6 entries) (2 entries)
Password@123


MPS CTC Jobs->list->timing
MPSCTC--> server name -> login credentials: Leelamar@16--->Administrator/Administrator

Mikes USCO Level DOAR

MPS CTC Portal-->link
iSRVE Bi Portal-->
iSRVE Jobs-->daily loads list
MPSBI Link->login credentials

uswu52965 / Aug@2014


MPSBI Daily Loads-->list
CSS-CPRS--> daily loads list (mon-sun)
WV Loads--> (sun-mon)
MSS Attinuity link-->
Tickets in new satate(just add this as new row)
Tickets missing SLA for today-same as above





phnx_report_service_request_xm




ORA-20999: Error: XSAT tables are not successfully refreshed for the day -1422ORA-01422: exact fetch returns more than requested number of rows
ORA-06512: at "XSATDW.PHX_JOB_CONTROL_PRC", line 15
ORA-06512: at line 1



----------step for mpsbi when asset uptime fails --at post process
nohup sqlplus -s mpsdm/skyfall#2012@MPSP @postprocess.sql > /home/mpsprd/log/ASSETUPTIME/postprocess_new.log &








runowb OWB_RT FUSION_PF_LOC PROCESS PHX_MASTER_LOAD_PF , ,
sleep 600
runowb OWB_RT FUSION_PF_LOC PROCESS PHX_EXP_REP_MASTER_LOAD_PF , IN_EFF_DATE=$PHNXDT
runowb OWB_RT FUSION_PF_LOC PROCESS PHNX_SSS_MASTER_LOAD_PF , IN_EFF_DATE=$PHNXDT
touch /home/isrveprd/bin/FIELD_OPS_HANDSHAKE_PHNX

3:59 PM 9/24/2013


----------pervasive
http://usa0300vm534:8181/Designers/IntegrationManager.html
1:30 PM 9/25/2013



update ISRVEDW.MSS_EXCESS_STG set STATE=trim(STATE) where length(state)>2 ; 

commit;



-----------query to give IT SERVICE COMPONENTS APPLICATION WISE--------------
select IT_SERVICE_ID,NAME from ximdw.CDP_IT_SERVICE_STG1 where it_service_group_id = 22 and assigned_group=22

1:06 PM 10/1/2013


ORA-20999: Error in SNMDM.USCO_SCR_DLYSUMMET_UPD_PRC100ORA-01403: no data found
ORA-06512: at "SNMDM.USCO_SCR_DLYSUMMET_UPD_PRC", line 1800
ORA-06512: at line 1



-----cron-----
Username : w3m9bxrj
Password  : Aug@2014 ( U capital)



----cpweb
 cpweb.opbu.xerox.com
  gdeeti / Apr@2014
su_usageprf / Apr@2014
----------331 server logs to be deleted---------
D:\Program Files\netegrity\webagent

---------qry to get last DML performer on table------

select max(ora_rowscn), scn_to_timestamp(max(ora_rowscn))
  from USWU47296.ISRVE_JOBS_MAST
--------qry to chk supplies pdw2 tables-----
SELECT * FROM  WHISC.WHISC_LOG@PDW2.WORLD WHERE TABLE_NAME LIKE 'SUPPLY_DEMAND_DAILY' and input_date = trunc(sysdate) ORDER BY JOBNAME DESC

select aa.*, to_char(input_date,'DAY')
  FROM WHISC.WHISC_LOG@PDW2.WORLD  aa
WHERE TABLE_NAME LIKE 'SUPP_OTCP_ORDER_INFO' /*AND
       INPUT_DATE SELECTDESC= TRUNC(SYSDATE)*/
       --and to_char(input_date,'DAY') like '%MONDAY%'
ORDER BY INPUT_DATE desc



Need to stop the Supplies Job for 1st Aug,2013 which is schduled at 4:00 AM and run it after 
9:30 AM EST since PDW2 jobs are getting delayed on workday 1 of every month.
11:06 AM 10/14/2013



response --

679658--NA
665969--NA
674402--NA
627493--NA


resolution--
679658--
663610
662646
--------
isrve_refresh_Weekly_radar

RDR_WEEK_SELECTION_PF 


USCO_SCR_MPL_DAILY_UPD_PRC
ORA-20999: Error in usco_scr_mpl_daily_upd_prc-30926
ORA-30926: unable to get a stable set of rows in the source tables
ORA-06512: at "SNMDM.USCO_SCR_MPL_DAILY_UPD_PRC", line 2669
ORA-06512: at line 1


698101--

exec sys.update_itt('698101');


update level 5 of TS from pulse stg
trunc(sysdate,'MM')


RDR_WEEK_SELECTION_PF :
USCO_SCR_MPL_DAILY_UPD_PRC 



exec sys.update_itt('698101');

exec snmdm.USCO_SCR_MPL_DAILY_UPD_PRC;

----------
 
SQL> set timing on;
SQL> set echo on;
SQL> set serveroutput on;
SQL> exec sys.update_itt('698101');
 
PL/SQL procedure successfully completed
 
Executed in 0.952 seconds
 
SQL> exec snmdm.USCO_SCR_MPL_DAILY_UPD_PRC;
 
PL/SQL procedure successfully completed
 
Executed in 318.179 seconds
 
SQL> 
-----------
NAME
EPR_UNIT_CANCELS_LP_PRC
EPR_UNIT_CANCELS_UPD_RSTMT_PRC
USCO_SCR_METRICS_F_LOAD_PRC
USCO_SCR_MPL_DAILY_UPD_PRC
USCO_SCR_MPL_UPD_PRC
USCO_SCR_BACKLOG_UPD_PRC
USCO_INDUSTRY_FILTER_RSTMT_PKG
USCO_LAND_PG_MET_UPD_PRC
USCO_SCR_UPD_HR_DATA_PRC
USCO_SCR_XNAO_PKG
USCO_SCR_XNAO_PY_UPD_PRC
USCO_SIGNINGS_METRICS_UPD_PRC
USCO_MS_MPL_DAILY_UPD_PRC


-------
678712 
679539 
684461 




NOTE:671434 
     687259 

----------
1. need to uncomment MSS loads..
2. need to complete mss loads.
3. SOF need to complete
4. PF_XGS_CDM_FINANCIAL laod 
5. delay mail for mss
SOF_LOAD_PART_DESC_PF

657760
------657760  old rfa XGS CDM FINANCIAL LOAD-----------need to chk imp

------new RFA
PF_XGS_CDM_FINANCIAL_LOAD : XGS_CDM_FINANCIAL_STG_PRC executed with below errors :

ORA-20005: Exception in  XGS_CDM_FINANCIAL_STG_PRC:-1502ORA-01502: index 'XGSDW.CPSL_METRIC_IDX' or partition of such index is in unusable state
ORA-06512: at "XGSDW.XGS_CDM_LOAD_PKG", line 155
ORA-06512: at line 1


--------OLD RFA 
1st Issue : PF_XGS_CDM_FINANCIAL_LOAD : XGS_CDM_FINANCIAL_STG_PRC executed with below errors :

Exception in XGS_CDM_FINANCIAL_STG_PRC:-1502ORA-01502: index 'XGSDW.CSPL_YR_IDX' or partition of such index is in unusable state

ORA-06512: at "XGSDW.XGS_CDM_LOAD_PKG", line 152

ORA-06512: at line 1 
 
 
-----OLD issue----------
XGSDW.CSPL_YR_IDX 
XGSDW.CPSL_METRIC_IDX 
XGSDW.CPSL_ACCOUNT_IDX 
XGSDW.CPSL_REV_COST_IDX 

------NEW issue-----------

XGSDW.CPSL_ACCOUNT_IDX 
XGSDW.CPSL_REV_COST_IDX 
XGSDW.CPSL_METRIC_IDX 
----
ORA-30926: unable to get a stable set of rows in the source tables


ticket for deployment

---inc serv of mss ticket-- send mail

outages

XGS_LEAD_SIGNING-- need to check trg file and RFA,

mail to cdp ticket...
b_MAIN_ODS_MPSCTC


PF_LOAD_MASTER_SUPPLIES 

XSBI PA Down and GA as well on 6-sep-2013
---------xsbi DL...
DL’s communicated : USA BI DW PROD SUPPORT; DL-TSG-OPS ; eppic24; Kelly, Bill; Labuhn, Ryan; Krishnasamy, Ramesh; Boswell, Jason ; Hoeppner, Sheila ; USA ECA Reporting 

All


MPSBI-- y3pb1qn3/Apr@2014---uma cred
---------------------

MPS -- ASSET_UPTIME_MTHLY_F load process failed. with below error:


/home/mpsprd/log/ASSETUPTIME--> cat postprocess.log
declare
*
ERROR at line 1:
ORA-00054: resource busy and acquire with NOWAIT specified or timeout expired
ORA-06512: at line 17
---------------------
nohup sqlplus -s mpsdm/skyfall#2012@MPSP @postprocess.sql > /home/mpsprd/log/ASSETUPTIME/postprocess_new.log &
11:34 AM 10/21/2013

usa7109eca.mail.xerox.com

13.41.230.150
------------NAF_DM.NAF_MV_REFRESH_PKG----------nagl details -----	

RCA for ops
incident MPL
.
PRAGMA AUTONOMOUS_TRANSACTION;--?


693686 --NAGL dblink used in report

-----------
usco_scr_new_ind_ids.sh
  /home/isrveprd/bin
  USCO_SCR_DAILY_PF:USCO_SCR_NEW_IND_IDS
----
SELECT   rec
    FROM (SELECT    industry_lvl1
                 || ','
                 || industry_lvl2
                 || ','
                 || created_dt
                 || ','
                                 || null AS rec,
                 2 AS ord
            FROM snmdm.usco_industry_lt
           WHERE UPPER (TRIM (industry_lvl1)) LIKE 'UNASSIGNED%'
          UNION
          SELECT 'Industry_Level1,Industry_Level2,Created_Date,New_industry_level1_value'        AS rec,
                 1 AS ord
            FROM DUAL)
ORDER BY ord;
---------
mc0300ux006% begin
*
ERROR at line 1:
ORA-00001: unique constraint (XSATDW.PK_REPORT_SR) violated
ORA-06512: at "XSATDW.LOAD_XSAT_MIR_TABLES_PRC", line 646
ORA-06512: at line 2


 Procedure failed

[1]    Done                 prd_daily_xsat_refresh

--------
ORA-01400: cannot insert NULL into ("XGSDM"."GDOB_REVN_FLASH_SUMM_F"."BILL_RUN_NO")


------------

ORA-20003: ERROR in phnx_sss_upd_prc-20003-ORA-20003: ERROR in XSATDM.xsat_call_detail_output_prc-29283-ORA-29283: invalid file operation
ORA-06512: at "SYS.UTL_FILE", line 536
ORA-29283: invalid file operation
ORA-06512: at "XSATDM.PHNX_LOAD_SSS_DATA_PRC", line 599
ORA-06512: at line 1




4:48 PM 10/28/2013


RDR_WEEK_SELECTION_PF
USCO_SCR_MPL_DAILY_UPD_PRC


insert:

snmdm.usco_scr_mpl_load_date_lt




set timing on;

set serveroutput on;
exec sys.update_itt('706859');

exec snmdm.USCO_SCR_MPL_DAILY_UPD_PRC; 




125929.-----prd_gldfeed_mjagtf




705900 
706062 
706173 
706268 






the scripts RFC_658700_inserts.sql
RFC_658700_TOC.sql
executed with errors in POST install steps

-------CAN PSC ERROR

ORA-20003: Error while executing ISRVEDM.CAN_PSC_PRE_OLS_LOAD_PRC-20001-ORA-20001: Error while generatring CANADIAN_FILE --29285-ORA-29285: file write error
ORA-06512: at "SATADMIN.OLS_CANADIAN_PKG", line 1696
ORA-06512: at "SATADMIN.OLS_CANADIAN_PKG", line 2510
ORA-06512: at "ISRVEDM.CAN_PSC_PRE_OLS_LOAD_PRC", line 17
ORA-06512: at line 1


---analysis
ISRVEDM.CAN_PSC_PRE_OLS_LOAD_PRC---> SATADMIN.ols_canadian_pkg.proc_run_canadian_pre_ols@ISRVETSPM.WORLD;


SATADMIN.ols_canadian_pkg-->proc_run_canadian_pre_ols


failed at ftp step --> SATADMIN.OLS_CANADIAN_PKG  line 2510---
ols_canadian_pkg.PROC_POP_CANADIAN_FILES(TRUNC(p_load_date),1);

--SATADMIN.OLS_CANADIAN_PKG,-->PROC_POP_CANADIAN_FILES line 1696

-----------where it failed
  select * from SATADMIN.CANADIAN_log_invitation--10 records
------------------------------------------------------------------------

SATADMIN.ols_canadian_pkg

.proc_run_canadian_pre_ols


 ols_canadian_pkg. PROC_UPD_load_control
 
 ----
 select * from  satadmin.canadian_load_control where load_id in (2,3,4,13);
 --REMARK---ftping FILe process Started
 
 ------
 
 SELECT length(comment_q17),length(comment_q18),length(q17),length(q18) FROM satadmin.canadian_response
	WHERE   1   =   1
	AND     TRUNC(CREATED_DT)   =   TRUNC(sysdate-1)
	AND     negative_indicator  =   'Y';--10 records
  
  
  select * from SATADMIN.CANADIAN_log_invitation--10 records--4.4  20C response file loaded successfully-29285-ORA-29285: file write error
  
  
  SELECT * FROM satadmin.CAN_PSC_OUTPUT_FILE_CTL WHERE OUTPUT_FILE_NO = 1 AND ACTIVE_IND='Y';--CC$PN.CCD13
  
  select LAST_DAY(ADD_MONTHS(SYSDATE-1,-1)) from dual
  select TRUNC(NEXT_DAY(LAST_DAY(ADD_MONTHS(SYSDATE-1,-1))-7,'FRIDAY'))
         from dual
         
select * from dba_directories  where    directory_name like '%CPSC%'    --/u25/ftp/ISRVE_FEEDS_OUT/CPSC


=----------------------------------------------------------




prd_equipment_perf_master
PHOENIX_MASTER_PF
  SVC_VARIABILITY_PF
  VBF_SUMMARY_MASTER_PF
  MSS_PRODUCT_FAMILY_PF
  MSS_MONTHLY_LOAD_PF
  MSS_SAR_MASTER_PF
  XGS_SUPP_MASTER_PF
  XS_FO_MONTHLY_PF
-----------

MSS_BPG_DAILY_MASTER_PF
MSS_BPG_DAILY_STG_LOAD_PF--failed at chn addr
MSS_BPG_DAILY_FACT_LOAD_PF


707780----

'28-OCT-2013'


exec sys.update_itt('707780');
exec isrve_utl.isrve_utl_pkg.ANALYZE_TABLE_PRC('ISRVEDW','MSS_ADDR_CHNG_STG',20); 


exec isrve_utl.isrve_utl_pkg.ANALYZE_TABLE_PARTITIONS_PRC('ISRVEDW','MSS_ORDER_BFE_STG','28-OCT-2013');

3:38 PM 10/30/2013





ORA-20999: ERROR IN xsatdm.phnx_load_hierarchy_prc -20003 - ORA-20003: ERROR IN xsatdm.phnx_load_hierarchy_prc-1-ORA-00001: unique constraint 

(XSATDM.PHNX_SSS_FLM_LT_IDX) violated
ORA-06512: at "XSATDM.XSAT_CALL_DETAILS_F_PRC", line 12
ORA-06512: at line 1





exec sys.update_itt('708433');


 select count(*)  from grsdw.GRS_V_HIST_STG where length(mach_sn) > 20; 

delete from grsdw.GRS_V_HIST_STG where length(mach_sn) > 20; 




PHNX_SSS_MASTER_LOAD_PF
PHNX_SSS_STG_LOAD_PF---ok ---ANALYZE_TABLE_PARTITIONS_PRC-- resubmittedable
PHNX_SSS_LT_DIM_LOAD_PF--failed--PHNX_LOAD_HIERARCHY_PRC---merge truncate insert

708781


planned outage for all 12:00 AM EST 5:00 AM EST 31st all application



--------------NAGL REFRESH ISSUE----------------
 select transaction_flag, count(*)
   from naf_dm.mvxcu0_centers_us
  group by transaction_flag;

if Y in null then run

exec sys.update_itt('709300');

exec naf_dm.mvxcu0_centers_us_act_flag_prc;
-----------------------------------

1:32 PM 11/11/2013
XPS_DAILY_PF--------

ORA-20005: SNMDW.XPS_DATACHK_PRC..-20005ORA-20005: ERROR OCCURED IN PROCEDURE SNMDW.XPS_DATACHK_PRC ..0ORA-0000: normal, successful completion
ORA-06512: at "SNMDW.XPS_DATACHK_PRC", line 24
ORA-06512: at line 1


swifs 
:


200 Port request OK.
550 No data sets found.
ftp> put sw410s.txt 'PROCH.SR.SR410S'
200 Port request OK.
125 Storing data set PROCH.SR.SR410S
250 Transfer completed successfully.
local: sw410s.txt remote: 'PROCH.SR.SR410S'
618140 bytes sent in 0.33 seconds (1814.39 Kbytes/s)
ftp> put sw420a.txt 'PROCH.SR.SR420A'
200 Port request OK.
125-Waiting for recall of data set PROCH.SR.SR420A
125 Storing data set PROCH.SR.SR420A
250 Transfer completed successfully.
local: sw420a.txt remote: 'PROCH.SR.SR420A'
1146435 bytes sent in 0.43 seconds (2603.37 Kbytes/s)
ftp> put sw420b.txt 'PROCH.SR.SR420B'
200 Port request OK.
125-Waiting for recall of data set PROCH.SR.SR420B
125 Storing data set PROCH.SR.SR420B
250 Transfer completed successfully.
local: sw420b.txt remote: 'PROCH.SR.SR420B'
3920350 bytes sent in 0.96 seconds (3987.36 Kbytes/s)
ftp> bye
221 Quit command received. Goodbye.


mv /u25/ftp/ISRVE_FEEDS_IN/FWSS85/fwss85.dat /u25/ftp/ISRVE_FEEDS_ARCHS/FWSS/fwss85.dat."`date +%Y%m%d`" 

mv /u25/ftp/ISRVE_FEEDS_IN/FWSS41/fwss41.dat /u25/ftp/ISRVE_FEEDS_ARCHS/FWSS/fwss41.dat.`date '+%Y%m%d%H%M%S'`

8:21 AM 11/13/2013







exec sys.update_itt('715712');


exec xgsdm.xgs_cdm_load_pkg.LOAD_PAGE_VOLUME_PRC('01-Oct-2013');
exec SNMDM.USCO_DELIVERY_PAGES_PRC('01-Oct-2013');

















S3 Name Email Address 
30164031 Mayrette D Balandra Mayrette.Balandra@xerox.com  
30164643 Jenny Velle V Mariano JennyVelle.Mariano@xerox.com  
30165938 Martin Allen D Sebastian MartinAllen.Sebastian@xerox.com  

 

 

Mirror ID:

 

30124174 / Christian Paul Mendoza / Christianpaul.mendoza@xerox.com

rdwh/ wordwide
 
kishore Hariram
ID: q3l44ql9  
Pass:Xerox@1234



"XGS_TOOLKIT_STRATEGIC_PKG"."TK_LOAD_FISH_INV_DAILY"();


isrve-- resolution - 5+0
        response -7+0







/home/mpsprd/ram/Releases_MPS_ER_15Nov/postinstall

MPSDM/skyfall#2012

chmod 755 mps_load_dimension_set_6.sh 
9:28 AM 11/17/2013



MCKB Dependent jobs:
XPS_DAILY_PF
CRS_ATTRIBUTE_INFO_DAILY_PF




ORA-01033: ORACLE initialization or shutdown in progress
ORA-02063: preceding line from MCKB
ORA-01033: ORACLE initialization or shutdown in progress
ORA-02063: preceding line from MCKB
ORA-06512: at "SNMDW.XPS_PROSPECTS_DAILY_STG_MAP", line 11
ORA-06512: at "SNMDW.XPS_PROSPECTS_DAILY_STG_MAP", line 1226
ORA-06512: at "SNMDW.XPS_PROSPECTS_DAILY_STG_MAP", line 1799
ORA-06512: at "SNMDW.XPS_PROSPECTS_DAILY_STG_MAP", line 5831
ORA-06512: at line 1

--------------------


17-NOV-

horly load triggered
Need to submit daily one
WV jobs
mps weekly loads need to ask deepak to start or not?
send status mail
cdp and mckb outage

30 17 * * * chkSchStatus DWHPSCH2_PF | $HOME/bin/dwhp_daily_2_schd.sh >>  $HOME/bin/dwhp_daily_2_schd.log--- if outage did not completes by 5 pm


00 08 * * * $HOME/bin/dwhp_daily_1_schd.sh >>  $HOME/bin/dwhp_daily_1_schd.log
00 12 * * * $HOME/bin/dwhpsch123.sh DWHPSCH2_PF >>  $HOME/bin/dwhpsch2.log
00 04 * * * [ `date | awk '{print $1}'` != "Sat" ] && $HOME/bin/dwhpsch123.sh DWHPSCH1_PF >> $HOME/bin/dwhpsch1.log













cdp jobs
mpsctc jobs

Oracle Warehouse Builder (OWB) - E0

9:21 PM 11/21/2013
RFA#727505--gdob
7:14 PM 11/25/2013



000-800-852-1308 


3--color n version
4--

ADRP Drill


RFA # 466669 has been raised for ISRVE DR  to support loads  executions on DR site. WO have been created for dev team. OWB functionalities to be  tested  on DR site. 
DR(Phase 2) with the DB & App Server DNS Switch for  Feeds/ETLs/Reports testing  on DR site was performed on June 15.
Ps team submitted ADRP documentation and plannoing a Platform DR on 12/14




Audit support ,logging and monitoring needs to be changed after confirming with DBAS



7--supplies ,usco --points
12--cdp issue
18--on dec 14 drill
14 RFA not matching with aopp code

2:24 AM 11/27/2013



679658--needs to remove CSE from isrve




Need to uncomment MSS loads.

-------report qry
 select a.scheduleid,a.lastextime,a.lastexstatus from rc_admin.botsched a ,rc_admin.botsit b
 where a.scheduleid=b.scheduleid and
b.intervaltype='D' and lastextime>trunc(sysdate)
select count(1) from rc_admin.botsched a ,rc_admin.botsit b
 where a.scheduleid=b.scheduleid and
b.intervaltype='D' and lastextime>trunc(sysdate)
---------REPORT CASTER LINK-------------

http://13.129.27.52:9120/ibi_apps/rcex.rc?is508=false&BIDrand=0.2396829252653922


------------MPS weekly job--------
30 17 * * 5 /home/mpsprd/bin/mpsIncidentFiller.sh  > /home/mpsprd/bin/mpsIncidentFiller.sh.log

need to check 'mps_load_incident_filler.complete' file in 
/home/mpsprd/bin/CTL_DIR









guiadmin.gui_reports--Y on releasing from report caster
----------Boxi long running reports------------
yBJ2LV7S
Eurasia shipments - OCF2425 12/2/13 3:31:00 AM Home/Prod/OPB/OMAR yBJ2LV7S  
-----------------------------------------------
733960



UPDATE  guiadmin.gui_reports 
    SET     max_data_date   = (SELECT MAX(post_period) FROM naf_dm.NAF_DTB_JOURNALS_MV), run_online = 'YES' 
    WHERE   report_id IN (639,640,641); 
    COMMIT; 
     
     
 
 exec sys.update_itt(733960); 
 



exec isrvedm.update_reporting_load_dates(635); 

 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(636); 
 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(637); 
 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(638); 
 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(639); 
 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(640); ---
 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(642); ---
 exec sys.update_itt(733960);
exec isrvedm.update_reporting_load_dates(641); 

-----------

PHX_EXP_REP_MASTER_LOAD_PF:

mc0300ux006% sqlplus

SQL*Plus: Release 11.2.0.3.0 Production on Tue Dec 3 08:27:06 2013

Copyright (c) 1982, 2011, Oracle.  All rights reserved.

Enter user-name: build_mgr@isrve
Enter password:

Connected to:
Oracle Database 11g Enterprise Edition Release 11.2.0.3.0 - 64bit Production
With the Partitioning, OLAP, Data Mining and Real Application Testing options

SQL> @usco_RFS_new_rfs_733037.sql;

------------crn------------
Areddy/Abcd_12345


mc0300ux006% crontab -l|grep cmss
##PA##00 04 * * 1-6 $HOME/bin/prd_daily_cmss.csh
1:15 PM 12/5/2013

report is in Account-site -> Pages report
  there is a shell script pg_acct_site.sh to run the procedure SNMDM.DATA_EXISTS_PAGE_VOL_PRC on the daily basis.
  this prc will check the data in the source tables and run the process flow PF_XGS_CDM_EQUIP_MASTER_PERF on data availability
  as of now in prod this PF got executed on 4th Dec, so this should load Nov data in PAges report
  but in Pages report still Data Load date is showing as 10/01/2013
  could plz check this..


7:25 PM 12/5/2013
---------ITSG

REPORT_ID	REPORT_NAME
691	ASP Labor Claim Address Report
692	Daily Claims Report
693	CCP Line Code Detail Report
694	CCP Line Code Summary Report
698	Work In Progress Onsite Jobs Report
699	Daily Shipment Recap By Service Provider Report


8:09 PM 12/11/2013



Falor, Mark A; Weissinger, Lyle; Burchett, Mark J
Simpson, Steve <Steve.Simpson@xerox.com>

Burchett, Mark J <Mark.Burchett@xerox.com>; Weissinger, Lyle <Lyle.Weissinger@xerox.com>; Falor, Mark A <Mark.Falor@xerox.com>


----------SLA response
704998
669146
710743
-------------
prd_workday_processing-->workday 2--> prd_equipment_perf_master-->prd_equipment_perf_master (last PF)
  /home/isrveprd/bin
--> PF_XGS_CDM_EQUIP_MASTER_PERF
mc0300ux006% crontab -l|grep pg_acct_site.csh
30 04 * * * $HOME/bin/pg_acct_site.csh



XS_FO_MONTHLY_PF
PF_XGS_CDM_EQUIP_MASTER_PERF

-----prd_monthly_cal_day_processing


prd_feeds_group_3
prd_post_load_lookup
-----------
From this query 6 MSS INV schedules are coming for Chris wing
  select a.schedule_id,a.saved_request_name,a.request_id ,a.report_id,B.REPORT_NAME,C.S3_ID,C.FIRST_NAME||', '|| C.LAST_NAME from isrvetools.reqparm a 
,GUIADMIN.GUI_REPORTS B,
ISRVETOOLS.USERS C
where a.schedule_id in (
select A.Schedule_Id from isrvetools.botlog_report a,rc_admin.botparms   b ,ISRVETOOLS.USERS C
where a.schedule_id=b.PARAM_SCHED
and b.param_name='REPORT_ID'
/*AND trunc(rundate)=trunc(sysdate)*/
AND UPPER(C.S3_ID)=UPPER(A.SCHEDULE_USER_ID)
and intervaltype='D'
/*AND ERROR_CODE=1*/
)
AND A.REPORT_ID =B.REPORT_ID
AND UPPER(A.CREATED_BY)=C.S3_ID
and C.S3_ID='US315734';

Query to get the report duration for chris wing and it shows 0 sec.
select A.* from isrvetools.botlog_report a,rc_admin.botparms   b ,ISRVETOOLS.USERS C
where a.schedule_id=b.PARAM_SCHED
and b.param_name='REPORT_ID'
--AND trunc(rundate)=trunc(sysdate-1)
AND UPPER(C.S3_ID)=UPPER(A.SCHEDULE_USER_ID)
and intervaltype='D'
and UPPER(C.S3_ID)='US315734'; 
---------------CPRS -- credential

 og89497
 Xerox@cprs
-------------iisreset.exe

2:56 PM 12/16/2013

12:02 AM 12/20/2013
-----------query to chk the rfc list for this ER--->Tracking current month RFC--in mks
select request_change_id,request_desc,(select name from ximdw.cdp_its_component_stg1 ss where ss.ITS_COMPONENT_ID=a.it_service_component) as comp from 

ximdw.cdp_rfc_stg1 a where IT_SERVICE_VERSION_ID=555941
 
u01/home/mpsiadmin/deployment_cvs/deployment_automation/

717605
731274
737990

-----------
'S17kr3fmujs5','S16ab5tmm3nc'
'S17tpmeti4bl','S17tr9pju8ci','S161j2f442ll','S15hdkp27nct'
'S16jov6cboli','S16jp0hbokm0','S16jov50f8lb','S16a1mgslt9v'
'S14r1n54idd0','S15akqmu8q8q','S17l05kg4f7k','Sf1616679sad32s4995sa30esee3973813bdd
'S15t2t1i1ms8','S15mid2d8e7b','S15micuvc578','S17tha5acb3k'
tempschedules:,'S17g32qm5j7u','S16e1pv69iu1','S1487h3525se','S16ga965gu11'
tempschedules:,'S16a1k19749l','S15t2t1hpps5','S15t2tcr6vsj','S1639e3hjc0f'
tempschedules:,'S1860n2goea0','S16rlcnfq2b5','S172prvmt35q','S14ido3cksgf'
tempschedules:,'S155dlhcqfbu','S14idnkjqtgc','S15sggeuki52','S15sggb1m84v'
tempschedules:,'S15mhtavoc4h','S1639ep7po13','S150dqqrs4it','S162a2u60qul'
tempschedules:,'S17d8u5hv48s','S165mg8hg83k','S16e29c2n0c8','S16a93tv439e'
tempschedules:,'S17heq0jpn9m','S1642k8iuso5','S173ekpmctsh','S17hhc0oc93h'


/home/mpsprd/ram/postinstall_DEC_Monthly--> jobs
[5] + Stopped (SIGTTIN)        nohup sqlplus -s mpsdm/skyfall#2012@MPSP @rfc_717605_mly_summ_f_load.sql>rfc_717605_mly_summ_f_load.log &
[4] - Stopped (SIGTTIN)        nohup sqlplus -s mpsdm/skyfall#2012@MPSP @rfc_717605_inc_ana.sql>rfc_717605_inc_ana.log &
[3]    Running                 nohup sqlplus -s mpsdm/skyfall#2012@MPSP @MPSDM.pi_RFC_731274_Activitydetmrg.sql>MPSDM.pi_RFC_731274_Activitydetmrg.log &
[2]   Stopped (SIGTTIN)        nohup sqlplus -s mpsdm/skyfall#2012@MPSP @rfc_717605_dly_summ_f_load.sql>rfc_717605_dly_summ_f_load.log &
[1]   Stopped (SIGTTIN)        nohup sqlplus -s mpsdm/skyfall#2012@MPSP @rfc_717605_upd_sla.sql>rfc_717605_upd_sla.log &




,ISRVE_BBL_USER

PHX_EXP_REP_SUMM_LOAD_PF


Steven.Reinsch@xerox.com

Steven.Reinsch@xerox.com


us981968

1:39 PM 12/26/2013

commented as part of RFC#692011 --
run_radar_prev_week_load

DI: 745998

746484 

Men are not prisoners of fate, but only prisoners of their own minds.

isrvedm.daily_district_cse 
isrvedm.daily_district_cse t 

select * from xgsdw.gdob_revenue_stg where load_date = (select max(load_date-2) from xgsdw.gdob_revenue_vw)

xgsdw.gdo_bill_rev_pkg--727505 RFA

usog87023
Password@03


------------trigger files for XGS_LEAD_SIGNINGS----------
/u25/ftp/ISRVE_FEEDS_IN/GDO/TNA_XSXS_ALLMTHS.trg

/u25/ftp/ISRVE_FEEDS_IN/GDO/XGS_CDM_ESTAB.trg-

-------/home/mpsprd/bin/dailyUptimestgLoad.ksh
  /home/mpsprd/bin/mpsAssetFillerLoad.sh

748009-IMP need to complete after USCO








sftp> lcd /u25/ftp/ISRVE_FEEDS_IN/XSAT/
sftp> cd /home/commsvcs/XSAT/
sftp> put XSAT_CALL_DETAIL_QUERY.csv*
Uploading XSAT_CALL_DETAIL_QUERY.csv.20140109 to /home/commsvcs/XSAT/XSAT_CALL_DETAIL_QUERY.csv.20140109
sftp> bye





mss/usco/


1 delay in bcc giri/anil pls validate n send it to user before 3

2 /nagl release

monthly load vallidation --mpp not opening

nagl --only morning r k confirm

snd mail to users if refresh goin long

nohup sqlplus -s build_mgr/frozen#nov2013@isrveprod @RFS_752644.sql > RFS_752644.log &

----------------------
select * from ximdw.CDP_REQUEST_TYPE_RELATIONS_LT   


------------------
select * from rc_admin.botsched where notify_subject = 'daily sumrray automatic report failed'
MSS_MREAD_DAILY_LOAD_PF 
CMSS_MREAD_DAILY_LOAD_PF

--------CDP Tier2 contact----
McCoy, David E <David.McCoy@xerox.com>



-----
711790 --fwss21.dat issue



Cheryllee.Davenport@xerox.com
Cheryllee.Davenport@xerox.com
-----------


select *
  from rc_admin.botlog2
 where stat_bt_name in
       (select stat_bt_name
          from isrvetools.botlog_report
         WHERE schedule_id in
               (select scheduleid
                  from rc_admin.botsched
                 where notify_subject =
                       'daily sumrray automatic report failed')
           and trunc(rundate) = trunc(sysdate - 20))
------------
usco jobs and reports:

select * from snmdm.usco_gui_reports_lt
--------




ORA-20001: Error while loading data to GDO Fact table - ORA-20001: Error while identifying source table date - ORA-28500: connection from ORACLE to a non-Oracle system 

returned this message:
[Microsoft][ODBC SQL Server Driver][TCP/IP Sockets]ConnectionRead (recv()). {01000,NativeErr = 65534}[Microsoft][ODBC SQL Server Driver][TCP/IP Sockets]General network 

error. Check your network documentation. {08S01,NativeErr = 11}
ORA-02063: preceding 2 lines from ISRVE_GDO_HS
ORA-06512: at "XGSDW.GDO_BILL_REV_PKG", line 498
ORA-06512: at line 1

-----------

ISRVEDM.ADP_HR_LOAD_PKG.MAIN('ADP_HR_TURNSTILE')


-----user portlets
select * from ISRVETOOLS.PORTAL_SCORECARD_PORTLETS

select * from ISRVETOOLS.PORTAL_USER_TABS where s3_id = 'USOG87023'






BEGIN DBMS_SESSION.CLEAR_IDENTIFIER(); END;
mv usco_finance_data.csv /u25/ftp/ISRVE_FEEDS_ARCHS/USSG/










ORA-20999: Error during data load to cdp_metric_detail_f-1400ORA-01400: cannot insert NULL into ("XIMDM"."CDP_METRIC_DETAIL_F"."REQUEST_STATE_ID")
ORA-06512: at "XIMDM.CDP_METRIC_DETAIL_INCIDENT_PRC", line 169
ORA-06512: at line 1

XIMDM.CDP_METRIC_DETAIL_INCIDENT_PRC
----------
CDP MIRROR:USA XOG DBA <USA.XOG.DBA@xerox.com>


2:55 PM 2/3/2014

5:59 PM 2/4/2014

CDP all jobs:

# Script for CDP Job - sch 11_02_2009
#It's a 4 Hrs CDP Refresh
15 00,04,08,12,16,20 * * * $HOME/bin/cdp_apsm_refresh.sh
#It's a 15 minutes CDP refresh
15 2,3,9,11,13,14,15,17,18,19,23 * * * $HOME/bin/cdp_realtime_refresh.sh
45 00,1,2,3,4,5,10,11,12,13,14,15,16,17,18,19,20,21,23 * * * $HOME/bin/cdp_realtime_refresh.sh
00 00,1,2,3,4,10,11,12,13,14,15,16,17,18,19,20,21,22,23 * * * $HOME/bin/cdp_item_refresh.csh
00 20 * * * $HOME/bin/cdp_mir_text_load.csh
## cdp AWPM refresh added on Sep 29 2011 as ER deployment
00 04 * * * $HOME/bin/cdp_awpm_refresh.sh
#script for cdp_apsm_monthly_refresh
15 1 1 * *  $HOME/bin/cdp_apsm_monthly_refresh.sh > $HOME/bin/cdp_apsm_monthly_refresh_log.log
30 13 * * * [ `date | awk '{print $3}'` -eq `cal | awk '{print $2 }' | grep . | fmt -1 | tail -1` ] && /home/isrveprd/bin/cdp_monthly_metrics.sh
## Added as part of RFC 207374 for CDP GRPS
00 00 * * * $HOME/bin/run_cdp_load_grps.sh
## added as part of CDP-ALM project - Apr 2012 monthly release
----------------------------------



Response--5
756510
730260
710459

resol--2
730260


total 7
Post sales revenue acess-------
-------
Connected to Oracle Database 11g Enterprise Edition Release 11.2.0.3.0 
Connected as build_mgr
 
SQL> set echo on;
SQL> set feed on;
SQL> select to_char(sysdate,'dd-mm-yyyy hh:mi:ss') from dual;
 
TO_CHAR(SYSDATE,'DD-MM-YYYYHH:
------------------------------
07-02-2014 11:47:22
 
SQL> exec sys.update_itt('768360');
 
PL/SQL procedure successfully completed
 
SQL> update SNMDM.USCO_SECURITY_LT set TIME_FRAME_IND = 1 where upper(seclt.S3_ID)='US991731';
 
update SNMDM.USCO_SECURITY_LT set TIME_FRAME_IND = 1 where upper(seclt.S3_ID)='US991731'
 
ORA-00904: "SECLT"."S3_ID": invalid identifier
 
SQL> update SNMDM.USCO_SECURITY_LT set TIME_FRAME_IND = 1 where upper(S3_ID)='US991731';
 
1 row updated
 
SQL> commit;
 
Commit complete
 

Connected to Oracle Database 11g Enterprise Edition Release 11.2.0.3.0 
Connected as build_mgr
 
SQL> set echo on;
SQL> set feed on;
SQL> select to_char(sysdate,'dd-mm-yyyy hh:mi:ss') from dual;
 
TO_CHAR(SYSDATE,'DD-MM-YYYYHH:
------------------------------
07-02-2014 12:26:50
 
SQL> exec sys.update_itt('768360');
 
PL/SQL procedure successfully completed
 
SQL> update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'CODE' where upper(S3_ID)='US991731';
 
1 row updated
 
SQL> commit;
 
Commit complete
 
SQL> update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'MANUALT',TIME_FRAME_IND = -1 where upper(seclt.S3_ID)='US991731';
 
update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'MANUALT',TIME_FRAME_IND = -1 where upper(seclt.S3_ID)='US991731'
 
ORA-00904: "SECLT"."S3_ID": invalid identifier
 
SQL> update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'MANUALT',TIME_FRAME_IND = -1 where upper(S3_ID)='US991731';
 
1 row updated
 
SQL> commit;
 
Commit complete
 
SQL> 
SQL> -------------
SNMDW.USCO_ORG_S3S_PRC
SNMDW.USCO_ORG_STG_LOAD_PRC
SNMDM.USCO_ORG_S3S_PRC--- to inser users from usco_org_s3s.csv file with time frame as 1
SNMDM.USCO_SECURITY_UPD_PRC
----------------------



Connected to 
Connected as build_mgr
 
SQL> set echo onl
SQL> set echo on;
SQL> set feed on;
SQL> select to_char(sysdate,'dd-mm-yyyy hh:mi:ss') from dual;
 
TO_CHAR(SYSDATE,'DD-MM-YYYYHH:
------------------------------
10-02-2014 11:26:20
 
SQL> set echo on;
SQL> set feed on;
SQL> select to_char(sysdate,'dd-mm-yyyy hh:mi:ss') from dual;
 
TO_CHAR(SYSDATE,'DD-MM-YYYYHH:
------------------------------
10-02-2014 11:27:25
 
SQL> select * from SNMDM.USCO_SECURITY_LT where upper(S3_ID)='US991731';
 
S3_ID                                              ACCESS_LEVEL                                       ACCESS_VALUE                                       ORG_TYPE_ID 

PROFILE_CD LOAD_TYPE  SECURITY_PROFILE_ID TIME_FRAME_IND
-------------------------------------------------- -------------------------------------------------- -------------------------------------------------- ----------- 

---------- ---------- ------------------- --------------
US991731                                           REP                                                1122AOM3                                                     2 

SVP        MANUALT                    999             -1
 
SQL> update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'CODE',PROFILE_CD = NULL,TIME_FRAME_IND=0 where upper(S3_ID)='US991731';
 
1 row updated
 
SQL> commit;
 
Commit complete
 
SQL> exec sys.update_itt('773907');
 
PL/SQL procedure successfully completed
 
SQL> 

Connected to 
Connected as build_mgr
 
SQL> set echo onl
SQL> set echo on;
SQL> set feed on;
SQL> select to_char(sysdate,'dd-mm-yyyy hh:mi:ss') from dual;
 
TO_CHAR(SYSDATE,'DD-MM-YYYYHH:
------------------------------
10-02-2014 11:26:20
 
SQL> set echo on;
SQL> set feed on;
SQL> select to_char(sysdate,'dd-mm-yyyy hh:mi:ss') from dual;
 
TO_CHAR(SYSDATE,'DD-MM-YYYYHH:
------------------------------
10-02-2014 11:27:25
 
SQL> select * from SNMDM.USCO_SECURITY_LT where upper(S3_ID)='US991731';
 
S3_ID                                              ACCESS_LEVEL                                       ACCESS_VALUE                                       ORG_TYPE_ID 

PROFILE_CD LOAD_TYPE  SECURITY_PROFILE_ID TIME_FRAME_IND
-------------------------------------------------- -------------------------------------------------- -------------------------------------------------- ----------- 

---------- ---------- ------------------- --------------
US991731                                           REP                                                1122AOM3                                                     2 

SVP        MANUALT                    999             -1
 
SQL> update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'CODE',PROFILE_CD = NULL,TIME_FRAME_IND=0 where upper(S3_ID)='US991731';
 
1 row updated
 
SQL> commit;
 
Commit complete
 
SQL> exec sys.update_itt('773907');
 
PL/SQL procedure successfully completed
 
SQL> select * from SNMDM.USCO_SECURITY_LT where upper(S3_ID)='US991731';
 
S3_ID                                              ACCESS_LEVEL                                       ACCESS_VALUE                                       ORG_TYPE_ID 

PROFILE_CD LOAD_TYPE  SECURITY_PROFILE_ID TIME_FRAME_IND
-------------------------------------------------- -------------------------------------------------- -------------------------------------------------- ----------- 

---------- ---------- ------------------- --------------
US991731                                           REP                                                1122AOM3                                                     2    

        CODE                       999              0
 
SQL> update SNMDM.USCO_SECURITY_LT set LOAD_TYPE = 'MANUALT',PROFILE_CD = 'SVP',TIME_FRAME_IND=-1 where upper(S3_ID)='US991731';
 
1 row updated
 
SQL> commit;
 
Commit complete
 
SQL> select * from SNMDM.USCO_SECURITY_LT where upper(S3_ID)='US991731';
 
S3_ID                                              ACCESS_LEVEL                                       ACCESS_VALUE                                       ORG_TYPE_ID 

PROFILE_CD LOAD_TYPE  SECURITY_PROFILE_ID TIME_FRAME_IND
-------------------------------------------------- -------------------------------------------------- -------------------------------------------------- ----------- 

---------- ---------- ------------------- --------------
US991731                                           REP                                                1122AOM3                                                     2 

SVP        MANUALT                    999             -1
 
SQL> exec sys.update_itt('773907');
 
PL/SQL procedure successfully completed
 
SQL> 

6:49 PM 2/17/2014


773952
774839

XISO-- Xerox Information Security office

xiso:
organisations info for security info(antivirus data on desktop)
source -share point(data providers, scorecard admin)
CIES_WKLY_INSTALL_SRVY_LOAD_PF


d /u25/ftp/ISRVE_FEEDS_OUT/CIES/ touch cies_bounce_bk_trg chmod 644 cies_bounce_bk_trg 


u25/ftp/ISRVE_SFTP_SCRIPTS/cies_sftp.


cd /u25/ftp/ISRVE_FEEDS_OUT/CIES/
touch cies_bounce_bk_trg
chmod 644 cies_bounce_bk_trg


/u25/ftp/ISRVE_SFTP_SCRIPTS/cies_sftp.sh--->

sftp iadmin@usa0300ux321.apps.mc.xerox.com <<EOF
lcd /u25/ftp/ISRVE_FEEDS_OUT/CIES/
cd  isrveSurveys
put cies_bounce_bk_trg
bye




mv /u25/ftp/ISRVE_FEEDS_OUT/CIES/cies_survey_match_feed /u25/ftp/ISRVE_FEEDS_ARCHS/CIES/cies_survey_match_feed.`date '+%m-%d-%Y-%T'`;
mv /u25/ftp/ISRVE_FEEDS_OUT/CIES/cies_journal_feed /u25/ftp/ISRVE_FEEDS_ARCHS/CIES/cies_journal_feed.`date '+%m-%d-%Y-%T'`;




mv /u25/ftp/ISRVE_FEEDS_OUT/CIES/cies_survey_match_feed /u25/ftp/ISRVE_FEEDS_ARCHS/CIES/cies_survey_match_feed.`date '+%m-%d-%Y-%T'`;
mv /u25/ftp/ISRVE_FEEDS_OUT/CIES/cies_journal_feed /u25/ftp/ISRVE_FEEDS_ARCHS/CIES/cies_journal_feed.`date '+%m-%d-%Y-%T'`; 
764907
773952
-----isrvetools-----
Users
Users_Groups                                                 
Attributes
Security_Values
Security_Attributes
Security_Alias
Security_Exemptions
User_Functioonalities
Functionalities
User_ Functionalities_Restrict
Categories_Groups
Group_Functionalities
------------
12:11 AM 2/21/2014


ftp_ussg/summer#2010
sh xeroxdeployment.sh

mpsiadmin
tcsps2012


sh backout.sh O


--------
 SELECT USERENV('TERMINAL') "Language" FROM DUAL;

4:43 PM 2/26/2014


------------CDP active users---------------
select * from XIMDW.MIR_MKSDOMAINGROUPMEMBERS where (groupname) like 'BI Prod Support'


SELECT SUM (BILLED_REVENUE), TRUNC (LOAD_DATE) FROM XGSDW.GDOB_REVENUE_VW WHERE TRUNC (LOAD_DATE) = :B1 GROUP BY TRUNC (LOAD_DATE)
SELECT DISTINCT BILL_RUN_NO FROM XGSDW.GDOB_REVENUE_VW

4:26 PM 3/4/2014

7:46 PM 3/8/2014
Inquisite Version 9.0-- already there 641211(D/F)
            PL/SQL Cartridge --
             need to 768094
            BOXI R2--

column D -- 1 RFA
      Oracle10.2.0.3 -EDW 641230
10:38 AM 3/20/2014

all US/CA users
isrved.ISRVE_EPIW_F
3:38 PM 3/26/2014

select * from owbsys.ALL_RT_AUDIT_MAP_RUNS order by created_on desc---query to get mapping execution
 select * from owbsys.ALL_RT_TASKS --- > all objects in OWB
select * from owbsys.ALL_RT_OBJECTS order by DEPLOYMENT_DATE desc ---> recently deployed PFS


DBA_UPDATABLE_COLUMNS ---table which shows whether view can be updated or not?




night shift NAGL query


select param_value ,min(duration),max(Duration),avg(Duration),count(*) from  isrvetools.botlog_report a,rc_admin.botparms   b ,ISRVETOOLS.USERS C
where a.schedule_id=b.param_sched
and b.param_name='REPORT_ID'
and param_value in (635)
AND rundate between
to_date('4/01/2014 13:00:00', 'MM/DD/YYYY HH24:MI:SS') and
       to_date('4/01/2014 23:59:00', 'MM/DD/YYYY HH24:MI:SS')
AND UPPER(C.S3_ID)=UPPER(A.SCHEDULE_USER_ID)
and intervaltype='M'
group by param_value


SELECT  msi.segment1, cic.item_cost, cic.last_update_date, msi.description, count(RTRIM(mif.segment1))
      FROM inv.mtl_system_items_b@isrve2sof.world mif,
           xrx.txrsc0_solos_chain_dtl@isrve2sof.world scd,
           bom.cst_item_costs@isrve2sof.world cic,
           inv.mtl_system_items_b@isrve2sof.world msi,
           (SELECT organization_id
              FROM inv.mtl_parameters@isrve2sof.world
             WHERE organization_code = 'E10') mp
     WHERE scd.chain_inventory_item_id = cic.inventory_item_id
       AND mif.inventory_item_id = scd.inventory_item_id
       AND mif.organization_id = scd.organization_id
       AND cic.inventory_item_id = msi.inventory_item_id
       AND cic.organization_id = msi.organization_id
       AND mp.organization_id = cic.organization_id
       AND cic.cost_type_id = 1
     group by msi.segment1, cic.item_cost, cic.last_update_date, msi.description
    having count(RTRIM(mif.segment1)) > 1

3:59 PM 4/17/2014

-----------PDW2----------------
select
    source_name,
    source_table, 
    source_row_count, 
    target_row_count, 
    load_start_time, 
    load_completion_time, 
    load_completion_status
from isrve_utl.load_status_control a
inner join isrve_utl.source_map_control b
on a.source_id = b.source_id
inner join isrve_utl.mirror_table_control c
on a.source_id = c.source_id
and a.mir_id = c.mir_id
where a.source_id = 4
and trunc(load_start_time) = trunc(sysdate);

-----


1:11 PM 4/21/2014
------------MCKB details
SELECT * FROM ISRVE_UTL.SOURCE_MAP_CONTROL
WHERE SOURCE_NAME = 'MCKB'


SELECT * FROM ISRVE_UTL.MIRROR_TABLE_CONTROL
WHERE TARGET_TABLE = 'MCKB.ORDER_FORECAST'
12:04 AM 4/29/2014

/u25/ftp/ISRVE_FEEDS_IN/SERS-->SERS.DAT-->SERS_EXT-->LOAD_SERS_VW-->LOAD_SERS-->EQUIPMENT(truncate insert)




-------------query to get the actual count of reports to be released-------
select a.schedule_id,
       a.saved_request_name,
       a.request_id,
       a.report_id,
       B.REPORT_NAME,
       C.S3_ID,
       C.FIRST_NAME || ', ' || C.LAST_NAME
  from isrvetools.reqparm a, GUIADMIN.GUI_REPORTS B, ISRVETOOLS.USERS C
 where a.schedule_id in (select distinct A.Schedule_Id
                           from isrvetools.botlog_report a,
                                rc_admin.botparms        b,
                                ISRVETOOLS.USERS         C
                          where a.schedule_id = b.param_sched
                            and b.param_name = 'REPORT_ID'
                               --AND trunc(rundate)=trunc(sysdate)
                            AND UPPER(C.S3_ID) = UPPER(A.SCHEDULE_USER_ID)
                            and param_value in (635)
                            and intervaltype = 'M')
   AND A.REPORT_ID = B.REPORT_ID
   AND UPPER(A.CREATED_BY) = C.S3_ID
---------------query to check reports saved/scheduled by user-------

SELECT R.*
  FROM ISRVETOOLS.reqparm R, rc_admin.botsit C
 WHERE  C.SCHEDULEID = R.SCHEDULE_ID
    and R.SCHEDULE_ID is not null
   and R.CREATED_BY = 'USX11594'
----------------------------------------------------------------
6:28 PM 5/13/2014

5:20 PM 5/16/2014

10:54 AM 5/30/2014
-----------------------query to get all grants related to any schema
 select dbms_metadata.get_granted_ddl('OBJECT_GRANT','BUILD_MGR') from dual;

9:46 PM 6/10/2014--------DBLINK---data
ISRVE_UTL.GEN_LOAD_SCRIPT_PRC
ISRVE_UTL.MIRROR_TABLE_CONTROL


---> to run the PF or map-->EXEC_OWB_MAP_PF_FUN
3:23 PM 6/27/2014

HC1_S_CONTRACTORS_CW---> will trigger automatically when Business places the file


rc_admin.botuprof---> save report is not working so need to have entry RFI#316345 
7:29 PM 7/10/2014


select * from dw_utl.DW_UTL_MASTER_LOG w
where process_owner='STG_POS'
and current_status='COMPLETE-ERR'
order by execution_start_date desc


-------if mps 4am job is long running
select  max("AuditDate")from mailto:dbo.rollupaudit@XRMWH20PROD.WORLD where "TableName" ='FWSSIncidentUptimes'


--------link to chke 4am job XSM side 
http://reporting.services.xerox.com/jobstatus/


-------------to chk 
SELECT DECODE (COUNT  , 0, 'Y', 'N')
     --INTO isLoadComplete
     FROM pervasive_admin.MPSBI_DA_FLAG@mps_vw.world
    WHERE     UPPER ("table_description") = 'ASSETUPTIME'
          AND "available_flag" = 'Y'
          AND TRUNC ("load_date") NOT IN
                 (SELECT load_date
                    FROM mpsdm.mps_assetuptime_load_dt_ctl
                   WHERE load_job = 'ASSETUPTIME');
-------------schedule control panel query-----------



SELECT   COUNT (DISTINCT c.param_sched) invalidcount, d.report_id
    FROM rc_admin.botparms@darsana_y c,
         isrvetools.reqparm@darsana_y d,
         rc_admin.botsched@darsana_y a,
         rc_admin.botsit@darsana_y b
   WHERE c.param_name = 't_rng'
     AND (   (TO_DATE (c.param_value, 'YYYYMMDD') <
                 (SELECT MAX (day_day)
                    FROM isrvedm.time_d
                   WHERE day_working_day_ind = 'Y'
                     AND day_day < TRUNC (SYSDATE))
             )
          OR c.param_value IS NULL
         )
     AND c.param_sched = a.scheduleid
     AND a.scheduleid = d.schedule_id
     AND a.scheduleid = b.scheduleid
     AND b.intervaltype = 'D'
     AND d.report_id IN ('641')
GROUP BY d.report_id

-----------table to get report error---

select * from guiadmin.schedule_request_log
-----iSRVE SAVE report funtionality-query to chk user able to save report in below security table--
select * from WFAPPL.wfsql_users where LOGIN = '30179850'
select * from WFAPPL.WFSQL_USER_GROUP where ID_USR = '1137386'--- 
-------------query to chk user able to save report in below security table------
select ID, lower(S3_id), FIRST_NAME, LAST_NAME
    from isrvetools.users a
   where a.s3_id = '30179850';
select b.id, a.id_group
            from WFAPPL.WFSQL_GROUPS a, isrvetools.users b
           where a.name = 'rc_group'
             and b.s3_id = '30179850';   



Christopher.Wing@xerox.com
12:56 PM 8/8/2014

5:45 PM 8/14/2014

1:11 PM 8/21/2014

3:05 PM 8/26/2014

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
-------------------------------------------------------------------------
--------------query to get it service and component----------
with rpt as
 (select c.*, rownum rn
    from (select A.NAME, CC.NAME as "COMPONENT"
            from ximdw.cdp_it_service_stg1 A,
                 (select *
                    from ximdw.cdp_its_component_stg1 c
                   where it_service_group_id = 22
                     and upper(STATE_DESC) = 'ACTIVE') CC
           where A.IT_SERVICE_GROUP_ID = 22
             and A.IT_SERVICE_ID != '364656'
             and A.IT_SERVICE_ID = CC.IT_SERVICE_ID
           order by A.NAME, "COMPONENT") c)
select case
         when A.NAME = b.NAME then
          ' '
         else
          A.NAME
       end NAME,
       A.COMPONENT
  from rpt a
  left outer join rpt b
    on a.rn = b.rn + 1
 order by a.rn;
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

-----------------------tuninig------------------------------------------------------------
http://docs.oracle.com/cd/B19306_01/server.102/b14211/sql_tune.htm
7:20 PM 9/17/2014
-------------query to get the list of all PFs in iSRVE------------------------------------
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

------------------------------------------------------------------------------------------
12:41 PM 10/21/2014

---------source standardization ---------
ISRVE_UTL.GEN_LOAD_SCRIPT_PRC
select * from   ISRVE_UTL.MIRROR_TABLE_CONTROL-----to check the tables are refreshed or not
select * from ISRVE_UTL.COLUMN_MAP_CONTROL 

1:31 PM 10/28/2014

------------------sql plan of sql-------'basic','ALL','TYPICAL'

select plan_table_output
  from v$sql s,
       table(dbms_xplan.display_cursor(s.sql_id, s.child_number, 'basic')) t
 where s.sql_text like '---select statement--%';


---------- BOXI Reports Audit-

9:10 PM 11/14/2014

q40rbv08
 )*Dec2014


Deeti, Giri Chaithanya?? [10:51 AM]:
 - login to 006 using your login
 - sudo login to isrveprd
 - type sqlplus
  ??Deeti, Giri Chaithanya?? [10:51 AM]:
 - give account name 'ps_mgr'
  - give existing password
  - type 'password'
  - will allow you to choose new password
  - validate new login after change, from plsql plus
  - share with team & ask shiva.g to update sheet


11:16 AM 12/8/2014


select * from nls_session_parameters

3:04 PM 2/16/2015

1:51 PM 2/17/2015
-------------------------------------
STEPS TO RUN C PROGRAM IN UNIX

create a file hello.c as below
******************************
#include<stdio.h>

main()
{
    printf("Hello World!");

}
******************************

compile the file using cc command
cc hello.c

********************************
a.out file will be generated

run this file as 
./a.out

-----------------------------------
owb_dc/PaSSword#2014@usa0300uz1303.apps.mc.xerox.com:1521:ISRVEQ

10:23 PM 3/18/2015

select * from TABLE(DBMS_XPLAN.DISPLAY('PLAN_TABLE','TSH','BASIC'));
select * from TABLE(DBMS_XPLAN.DISPLAY);
12:12 PM 4/8/2015

----------selecting .4 % of table---------
select * from table_name sample(0.4)
--------------------
  usageprf is the user
  cpbpunix123

9:20 PM 5/4/2015

SELECT * FROM table(DBMS_XPLAN.DISPLAY_AWR('atfwcg8anrykp')); ----- sql plan for hist

11:09 AM 6/11/2015

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

---------------------------------------------------------

•	RC_ADMIN.BOTTASK
•	RC_ADMIN.BOTPARMS
