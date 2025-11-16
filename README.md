Alexander Mihailov, 7 May 2025

This is the readme_GPStripes_EcolEcs_250507.txt file for the replication of "Greening Prosperity Stripes across the Globe", Ecological Economics, 2nd resubmission (April 2025).

Most data sources and links to the data are from the World Bank and provided in the article (with respective URLs). There are also data in the public domain from the UK Met Office, provided in the article too (with respective URLs).

There are 2 subfolders:

   STATANowSE185 -> This subfolder contains data and STATA (version Now SE 18.5) codes in a "replication" subfolder. It contains a separate readme file, readme_GPMaps_EcolEcs_replication.pdf. This STATA "replication" folder generates the world maps (i.e., figures 2 and 3 in the article, with winsorizing at 5% and 95%).

   MATLABR2023a -> This subfolder contains data and MATLAB (version R2023a) codes in a "replication" subfolder. Its content is described below. It generates the remaining graphs in the article.

In particular, there are 3 original *.xls files downloaded from the World Bank database online:

API_EN.ATM.CO2E.PC_DS2_en_excel_v2_5607813.xls -> World Bank CO2 emissions data API_NY.GDP.PCAP.CD_DS2_en_excel_v2_5607109.xls -> World Bank GDP pc data in USD of 2015 API_NY.GDP.PCAP.PP.KD_DS2_en_excel_v2_5607670.xls -> World Bank GDP pc data at PPP in international USD of 2017

There are 3 corresponding *.xlsx files with the same name, containing some minimal notes, marks and manipulations by me that were used for the MATLAB codes herein: note that MATLAB in Mac OS allows only working with *.xlsx files, not *.xls ones, so I had created the former from the latter:

API_EN.ATM.CO2E.PC_DS2_en_excel_v2_5607813.xlsx
API_NY.GDP.PCAP.PP.KD_DS2_en_excel_v2_5607670.xlsx

and 

API_NY.GDP.PCAP.CD_DS2_en_excel_v2_5607109.xlsx used for the GDPpcWorldUSDof2015.txt file explained below.

The 2 MATLAB code (*.m) files described below can be executed in arbitrary order. They use the above *.xlsx files to read from.

GDPpcCO2pcStripes1stSmpl4Groups8CountriesMinMaxWorld_am241007w5.m -> with winsorization at %5 and 95% as in the cross-section for 2020 (i.e., comparable with the respective winsorization in the STATANowSE185 folder)
GDPpcCO2pcStripes2ndSmpl2Groups10CountriesMinMaxWorld_am241007w5.m -> with winsorization at %5 and 95% as in the cross-section for 2020 (i.e., comparable with the respective winsorization in the STATANowSE185 folder)

The next 2 *.m codes,

GDPpcWorldUSDof2015Stripes_am231204.m
LifeExpectancyWorldStripes_am231204.m

use 2 *.txt files to read from (based, again, on the World Bank original data), namely,

GDPpcWorldUSDof2015.txt coming from the World Bank's API_NY.GDP.PCAP.CD_DS2_en_excel_v2_5607109.xls
LifeExpectancyWorld.txt coming from the World Bank's API_SP.DYN.LE00.IN_DS2_en_excel_v2_5607706.xls

Finally,

ClimateStripesReplication.m

uses the Met Office HadCRUT.5.0.1.0.analysis.summary_series.global.annual.txt data to replicate the climate stripes in the respective figure in the online appendix to the article.

The filenames of the *.m programs are self-explanatory. Each of them contains very detailed annotation and guidance.

The MATLAB R2023a programs generate all graphs for the figures in the main text and online appendix, as well as the necessary ingredients to compile (manually) Table 1.
