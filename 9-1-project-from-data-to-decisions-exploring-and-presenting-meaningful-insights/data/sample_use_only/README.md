# About the data

## 1_Sample_Initial_EDA
**titanic_raw**
This is a file obtained from the Kaggle entry level Titanic competition.
https://www.kaggle.com/competitions/titanic

**Provisional_COVID-19_Deaths_by_Sex_and_Age**
This is a sample dataset for a Federal provisional analysis of COVID-19 related deaths by State, Sex, and Age obtained from Data.gov.
https://catalog.data.gov/dataset/provisional-covid-19-death-counts-by-sex-age-and-state

**NCHS_-_Leading_Causes_of_Death__United_States**
This is a sample dataset of the reported cause of death of US citizens across the US as tracked by the US Department of Health and Human Services obtained from Data.gov.
https://catalog.data.gov/dataset/nchs-leading-causes-of-death-united-states

**Crime_Data_from_2020_to_present**
This is a sample dataset of the reported crime data within the City of Los Angeles since 2020 obtained from Data.gov
https://catalog.data.gov/dataset/crime-data-from-2020-to-present

business_data.csv
This is a sample business dataset from an unknown organization.

## 2_Sample_Data_Wrangling
#### Dirty Data Files

| File | Description | Source |
| --- | --- | --- |
| `business_data.csv` | Dirty business data from an unknown source | Adapted for this course from an undefined business |
| `dirty_data.csv` | 2018 weather data for New York City, manipulated to introduce data issues. | Modified version of the data from the NCEI API's GHCND dataset. |

#### Sources
- The National Centers for Environmental Information (NCEI) provides an [API](https://www.ncdc.noaa.gov/cdo-web/webservices/v2), which we use to access the [*Global Historical Climatology Network - Daily* (GHCND) dataset](https://www1.ncdc.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf).


## 3_Sample_Data_Blending_Preprocessing
##### Weather Data Files

| File | Description | Source |
| --- | --- | --- |
| `earthquakes.csv` | Earthquake data from September 18, 2018 through October 13, 2018. |  The US Geological Survey (USGS) earthquake API. |
| `nyc_temperatures.csv` | Temperature data for New York City in October 2018 measured from LaGuardia airport, containing daily minimum, maximum, and average temperature. | The NCEI API's GHCND dataset |
| `nyc_weather_2018.csv` | Long format weather data for New York City across various stations. | The NCEI API's GHCND dataset. |
| `parsed.csv` | Data from `earthquakes.csv` with an additional column for the location (parsed from the data to handle multiple names for the same entity). |  The US Geological Survey (USGS) earthquake API. |
| `quakes.db` | A SQLite database of a single table, `tsunamis`, which contains all data on the earthquakes in `earthquakes.csv` that were accompanied by a tsunami. |  The US Geological Survey (USGS) earthquake API. |
| `tsunamis.csv` | Data for all earthquakes in `earthquakes.csv` that were accompanied by a tsunami. |  The US Geological Survey (USGS) earthquake API. |
| `weather_by_station.csv` | Long format weather data for New York City across various stations, along with station information. | The NCEI API's GHCND dataset and the `stations` endpoint. |
| `weather_stations.csv` | Information on all the stations providing weather data for New York City. | The NCEI API's `stations` endpoint. |
| `weather.db` | The `weather` table contains New York City weather data, while the `stations` table contains information on the stations. | The NCEI API's GHCND dataset and the `stations` endpoint. |

## 4_Sample_Visualizations

We’ll use a database from NCES (National Center for Education Statistics) focusing on per-pupil spending by state.

The NCES collects this type of data through their "Common Core of Data (CCD)" system, specifically in the "National Public Education Financial Survey (NPEFS)" dataset. The most recent complete dataset can be found as:

**Table 333.30 - Appropriations from state and local governments for public degree-granting postsecondary institutions, by state or jurisdiction: Selected academic years, 1990-91 through 2020-21**

Link: https://nces.ed.gov/programs/digest/d22/tables/dt22_333.30.asp (hit “Download Excel” on this page to download dataset)
