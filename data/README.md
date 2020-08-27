# Data Sources: 
* **Daily reported COVID-19 cases and deaths collected by the New York Times.** 
  > county_deaths.csv

  Cases and Deaths are reported at the county level, across the USA. Data was downloaded from https://github.com/nytimes/covid-19-data on May 11, 2020.
* **COVID-19 deaths by race collected and reported by the CDC.** 
Data was collected and normalized by the CDC. It was downloaded on May 13, 2020 from: https://www.cdc.gov/nchs/nvss/vsrr/covid_weekly/index.htm
Importantly, the percentage of racial/ethnic groups per state population that is reported has been weighted. These weights ensure that the population estimates and percentage of COVID deaths represent comparable geographic areas. To see more details on how the weighted percentages were calculated, please visit: https://www.cdc.gov/nchs/nvss/vsrr/covid19/tech_notes.htm
* **Community-level vulnerability index scores reported by The Surgo Foundation.**  
  > county_ccvi.csv

    The Surgo Foundation has calculated scores to measure community-level vulnerability during a pandemic. This data was downloaded from https://precisionforcovid.org/ccvi     on May 12, 2020. These scores are based off of the CDC's Social Vulnerability Index (SVI) https://svi.cdc.gov/ but also include information on the underlying health       conditions and state of the community's healthcare system. To read more about these scores, please visit: https://medium.com/@surgofoundation/why-we-created-a-new-         vulnerability-index-specific-to-covid-19-3d88ce1de9ef. Specifically these scores are measures of: 
    * socioeconomic factors
    * household composition & disability
    * minority status & language
    * housing type & transportation
    * epidemiological factors 
    * healthcare system factors

* **Detailed demographic data at the county level from Johns Hopkins Univerisity.** 
Downloaded from: https://github.com/JieYingWu/COVID-19_US_County-level_Summaries/tree/master/data Dataset includes 347 features - demographic, socioeconomic, health care, education and transit data for each county in the 50 states and Washington DC. Note that this also includes analogous data for states, as available.


* county_detailed_demographics_and_deaths.csv
  
  For code on genrating this CSV, see [notebook: 'KM_merge_datasets_county_level_demographics_and_covid_deaths.ipynb'](https://github.com/kmussar/covid19_datathon/blob/master/eda/KM_merge_datasets_county_level_demographics_and_covid_deaths.ipynb)
    This CSV is the product of merging the following datasets on FIPS code. 
   * Detailed demographic data from Johns Hopkins University
   * COVID-19 deaths from The New York Times. Group the number of deaths by FIPS code.
   * Community-level vulnerability scores from The Surgo Foundation
