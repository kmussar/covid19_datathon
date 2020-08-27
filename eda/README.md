# Question: Which socioeconomic factors contribute most to racial disparities in morbidity from COVID-19?

# Data: 
* **Daily reported COVID-19 cases and deaths collected by the New York Times.** 
Cases and Deaths are reported at the county level, across the USA. Data was downloaded from https://github.com/nytimes/covid-19-data on May 11, 2020.
* **Community-level vulnerability index scores reported by The Surgo Foundation.**  
  The Surgo Foundation has calculated scores to measure community-level vulnerability during a pandemic. This data was downloaded from https://precisionforcovid.org/ccvi on May 12, 2020. These scores are based off of the CDC's Social Vulnerability Index (SVI) https://svi.cdc.gov/ but also include information on the underlying health conditions and state of the community's healthcare system. To read more about these scores, please visit: https://medium.com/@surgofoundation/why-we-created-a-new-vulnerability-index-specific-to-covid-19-3d88ce1de9ef. Specifically these scores are measures of: 
  * socioeconomic factors
  * household composition & disability
  * minority status & language
  * housing type & transportation
  * epidemiological factors 
  * healthcare system factors
* **Detailed demographic data at the county level from Johns Hopkins Univerisity.** 
Downloaded from: https://github.com/JieYingWu/COVID-19_US_County-level_Summaries/tree/master/data Dataset includes 347 features - demographic, socioeconomic, health care, education and transit data for each county in the 50 states and Washington DC. Note that this also includes analogous data for states, as available.

# Approaches:
## At the county level 
**Notebook: 'KM_merge_datasets_county_level_demographics_and_covid_deaths.ipynb'**
1. Load datasets: 
  * Detailed demographic data from Johns Hopkins University
  * COVID-19 deaths from The New York Times. Group the number of deaths by FIPS code. 
  * Community-level vulnerability scores from The Surgo Foundation 
2. Join the three datasets, join on FIPS code. 
**Resulting csv 'county_detailed_demographics_and_deaths.csv'**

## At the state level 

### Case Study - South Carolina and Tennessee
Approximately 30% of South Carolina and Tennessee's populations are Black. In Tennesse, about 30% of deaths due to COVID are in Black patients. However, in South Carolina, this rises to a disproportionate 53%. What differences in social vulnerability indexes do we find between these states? 
* Notebook: 'KM_SouthCarolina_Tennessee.ipynb'



# Future Directions
Filter the dataset to the counties where there is a disproportiate number of deaths in a certain ethnicity compared to the percentage of that ethnicity in the county. Use propensity scores to weight counties that don't have disparities, but are otherwise comparible, higher.

Read more about propensity scores to figure out where to go from there: https://www.rand.org/pubs/reprints/RP1252.html
