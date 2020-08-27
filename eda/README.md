# Question: Which socioeconomic factors contribute most to racial disparities in morbidity from COVID-19?

# Data: 
For a details on our data sources, please see the data folder in this repo. (https://github.com/kmussar/covid19_datathon/tree/master/data)  
* **Daily reported COVID-19 cases and deaths collected by the New York Times.** 
* **Community-level vulnerability index scores reported by The Surgo Foundation.**  
* **Detailed demographic data at the county level from Johns Hopkins Univerisity.** 

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
