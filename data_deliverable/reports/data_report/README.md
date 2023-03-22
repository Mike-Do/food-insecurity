# Data Report
Zambies 🧟

## Link to datasets: https://drive.google.com/drive/folders/1yroX_ttrxujoTq65cwatwcWZTfco6lCR?usp=share_link

----------------------------------------------------------------------------
## Format of Our Data
## For FAOSTAT Crops Dataset
The data is in the form of a CSV file. The data is in the form of a table, with each row representing a single record. The columns are as follows:
* `Country`: The country the record is from. It is a string. This is a required value that we joined our data on, and groups the data by country. We will use this to analyze the data by country.
* `Crop`: The production domain of the record represented as a string. This value holds the crop that the record is about, either "Maize," "Rice," or "Wheat." This is a required value that allows us to group our data by crop. We will use this to analyze the data by crop.
* `Year`: The single year the record is represented as an integer. This value ranges from 1990 to 2021. This is a required value that allows us to group our data by year, and make predictions about the future. 
* `Yield`: The yield of the crop in the given country in the given year. Measured in tonnes per hectare, it represents the harvested production per unit of harvested area for crop products.
Yield Minimum value: 0.0001261869459604404
Yield Maximum value: 36.76190476190476


* `Area Harvested`: The area from which the crop is gathered in the given country for the given year. Measured in hectares, it represents the area of land that is used for crop production.
Area harvested Minimum value: 0.0
Area harvested Maximum value: 48178000.0
* `Production`: The total production of the crop in the given country for the given year.Measured in tonnes, it represents the total domestic production whether inside or outside the agricultural sector, i.e. it includes non-commercial production and production from kitchen gardens.
Production Minimum value: 0.03
Production Maximum value: 412262180.0

## For F
Note:
We don’t have to use any of the fields to detect possible duplicate records, by nature of the datasets that we are working with in the first place (they’ve all been cleaned). But if we did have to account for duplicates, we would have to look at the country, crop, and year in conjunction.

### `Area/Country`
* Data type: String
* Default value: None
* Range of value: different countries (97 in total)
* Simplified analysis of the distribution of values: For FAOSTAT crops, there are the same number of entries for every country (with different entries corresponding to a given crop and year). For FAOSTAT indices, it seems that there are unequal numbers of entries in the dataset corresponding to different countries, probably because some indices aren’t associated with certain countries.
* Unique (Y/N): No
* Used (maybe in composition with others) to detect possible duplicate records (Y/N): No
* Required (Y/N): Yes
* To be used in the analysis (Y/N): Yes; the main goal of our project is to develop insights on the disproportionate impact of climate hazards on different countries, so the country itself is definitely relevant to our analysis.
* Contains potentially sensitive information (Y/N): No

### `Year`
* Data type: Numeric (Integer)
* Default value: None
* Range of value: 1990 - 2021
* Simplified analysis of the distribution of values: We’re looking at the range of years dating from 1990 to 2021.
* Unique (Y/N): No
* Used (maybe in composition with others) to detect possible duplicate records (Y/N): No
* Required (Y/N): Yes
* To be used in the analysis (Y/N): Yes; change over time, in relation to climate and food supply, is definitely relevant to our analysis, especially if we choose to add a predictive element for the machine learning portion of the project.
* Contains potentially sensitive information (Y/N): No

### `Crop`
* Data type: String
* Default value: None
* Range of value: 3 different crops (Maize, Rice, Wheat)
* Simplified analysis of the distribution of values: We are primarily analyzing these crops to get a generalized representation of a country’s food supply.
* Unique (Y/N): No
* Used (maybe in composition with others) to detect possible duplicate records (Y/N): No
* Required (Y/N): Yes
* To be used in the analysis (Y/N): Not directly; this will go toward an overall picture of a country’s food supply in a given time period, in response to a certain climate hazard.
* Contains potentially sensitive information (Y/N): No

### `Climate scenario`
* Data type: String
* Default value: None
* Range of value: 19 different climate scenarios
* Simplified analysis of the distribution of values: Different codes represent different climate scenarios, particularly pertaining to different greenhouse gas concentration pathways; for example, RCP2.6 represents a rapid and sustained reduction in future global greenhouse gas emissions resulting in an increase in global average temperature of around 2°C above pre-industrial levels by the end of the 21st century.
* Unique (Y/N): No
* Used (maybe in composition with others) to detect possible duplicate records (Y/N): No
* Required (Y/N): Yes
To be used in the analysis (Y/N): Yes; this will likely be our main representation of climate scenarios for the “climate change” aspect of our project.
* Contains potentially sensitive information (Y/N): No
