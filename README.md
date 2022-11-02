# TestProg_ReportCruncher
Tool to maintain and improve(2007-2011). 
The purpose of this was to take in 2 sets of validation data and extract the Pass and Failures over the same positions and show it in an overview with graphs.

---------------------------------------------------------------

'User Notes:

'Requirements to use this tool.
'(24 Nov 2008)
'1) If Downbin data is needed to be included in this data. Please use DownBinExtractAll tool 1st before using this macro.
'2) Accepts health ,ohayo and other csv files data(provided the headers must be the same) but must only provide a maximun of 84 position data for each run
'3) User are advised to follow the given template for both static and actual Main/production data.
'4) Please when using input the require data, follow the way the buttons are located on the form. From top to bottom.

'(05 Dec 2008)
'1) Able to plot the below 3 charts:
'   a) HSLT Non-Repeated Down Bin Failures
'   b) HPBI Non-Repeated Down Bin Failures
'   c) HSLT Non-Repeated Inconsistence Failures
'
'2) Must use the new perl script(HPBIcheck.pl instead of DownBinExtractAll.pl) before using this Macro.
'   The new tool will extract all HSLT and HPBI downbins test failures/details.

'3) User can define the failure description for Failcharting by keying the Identifier 1 and 2(Sheet refernce)so that the macro
'   can reference to when looking for the specific key words as given and be replace with the ones in remarks. The Macro will also
'   "grab" the required data as specific in Identifier 2 to be added to remarks.
'
'4) Script headers reference are hardcoded base on Health header names like:
'       Fail detail
'       Tprog Filename
'   Thus, the script will not work if an unknown similar header is being used instead.
    
'(26 Feb 2009)
'1) Inconsistance Failure details will be compare for the 3 runs to see if there are duplicates by
'   comparing their softbin. (HST-3952)
'2) HSLT downbin failure details comes with failure type. (Eg. WIN_SETI: Correctable MCA)
'   New version of HPBIcheck_v2.pl has been updated with this feature.(HST-3951)
'3) Chart ploting has been change to horizontal bar chart with legend show.

'(18 Mar 2009)
'1) Added condition to dealt with cases where some tprogs files are missing and will cause an endless loop. (Mod3, HPBIbin)
'2) Failure details code edited to enable "Delta" details appending in the final failure description. (eg. Delta Alarm 8 - DUT_ERR_THMAX)

'(22 May 2009)
'1) Added in the default headers in Temp sheets so user dont need to select the require headers.

'(30 Jul 2009)
'1) HST-5526. Script/Macro Development for automated data extraction and graph creation - Failure Pareto Chart to be displayed Horizontally

'(20 Aug 2009)
'1) HST-5526. Script/Macro Development for automated data extraction and graph creation - Failure Pareto Chart to be displayed Horizontally
'2) HST-3946. Script/Macro Development for automated data extraction and graph creation - Additional KPI Table

'(25 Aug 2009)
'1) HST-5809. Scrip/Macro Development for high level repeatability calculation
'2) HST-3946. Script/Macro Development for automated data extraction and graph creation - Additional KPI Table

'(08 Dec 2009)
'1) HST-5979. Fix the SB issue to correct the Macro inconsistance Failures charting to make it compatible  with the new SB (7digits).
'Make the macro look at HB for all failing bins (15 or unknown) then check if any SB is diff to grep the inconsistence Failures.

'(01 Feb 2010)
'1) Bug Fix reported by Nyan Lin: Inconsistance Failure did not work due to hardcoded headers.
'2) Add in text comments on sheet TMP to inform users to amend the headers list as required.


