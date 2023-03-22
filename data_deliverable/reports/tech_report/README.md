# Tech Report
There are a large amount of data points throughout our datasets. This should be enough data to train a model that can predict metrics of a crop in a given country for a given year in our analysis.
There are 12858 rows in our pre processed FAOSTAT crop dataset
There are 4488 rows × 34 columns in our preprocessed FAO Food Insecurity Indicators dataset


## Data Description
The identifying attributes are `Country`, `Crop`, and `Year`. These are the attributes that we will use to group our data by. We will use these attributes to analyze the data by country, crop, and year, and their respective yields, area harvested, and production. These give us a concrete idea of food security in a given country, and how it has changed over time.
In the Food Insecurity dataset, the identifying attributes are “Country” and “Year”, among with 32 columns that are indicators of food insecurity according to FAO (for example, GDP, % of population with access to clean water, etc) 


## Data Sources
The three data sources for this project are from [FAOSTAT crops and livestock products] (https://www.fao.org/faostat/en/#data/QCL), [FAOSTAT Food Security and Nutrition Indicators] (https://www.fao.org/faostat/en/#data/FS), and a (Global Dataset) [https://www.nature.com/articles/s41597-022-01150-7] built from 202 studies published between 1984 and 2020. FAO is the Food and Agriculture Organization of the United Nations, and is a specialized agency of the United Nations that leads international efforts to defeat hunger. They collect their data from national statistical agencies, international organizations, and other sources via Questionnaires. This data is widely used in the field of agriculture and food security, and is a reliable source of data for our project. The Global Dataset is constructed and used by the Intergovernmental Panel on Climate Change (IPCC), an intergovernmental body that provides the world with a clear scientific view on the current state of climate change and its potential environmental and socio-economic consequences. The IPCC is the leading international body for the assessment of climate change, and is also a reliable source of data for our project. We generated our data by selecting columns relevant to our analysis, and joining the data on `Country`.


## Cleaning the Data
Cleaning data: drop irrelevant columns and renamed them (documented in our notebook)
Projected dataset, replaced with 0
The food insecurity dataset initially had 52 features,, but some of them had the majority of entries as missing (NaN) values. These columns were removed due to a lack of workable data. Additionally, some of the year data was given in three-year averages, and the year column was changed to match the first year of the averaged period. 
There are some missing data points in the FAO Food Insecurity dataset, particularly for more recent years. We can navigate these gaps by either not looking at the most recent years, or by trying to predict this missing data as part of our goals for the machine learning aspect of the assignment. 


## Observations and Challenges
When calculating the range for the crop FAOSTAT data, we determined that there were values of “infinity” in Yield, most likely due to a division error.

Furthermore, we had trouble narrowing down the set of inputs that we would ultimately use toward our visualization / machine learning predictions. As a result, we had a pretty large dataset with as many inputs as we could see ourselves using, and we plan to use what we need when we come up with a clear hypothesis.

## Summary
Collecting our data has allowed us to narrow down our scope of questions for the analysis portion of the assignment. The prevalence of predicted crop data and climate change data could allow us to do a time-series analysis / predictive machine learning model problem where we predict various food insecurity indicators based on the future crop/climate data. Additionally, due to the large amount of intersecting data for a specific country and year, we could do some interesting unsupervised learning tasks to find patterns and correlations between the different data sets and food insecurity areas.
