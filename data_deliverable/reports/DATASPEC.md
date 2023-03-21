Type of data that will be used for the representation.
Default value
Range of value.
Simplified analysis of the distribution of values
Are these values unique?
Will you use this value (maybe in composition with others) to detect possible duplicate records? If so, how?
Is this a required value?
Do you plan to use this attribute/feature in the analysis? If so, how?
Does this feature include potentially sensitive information? If so, how do you suggest handling such issues?


# Data Report

Zambies 🧟

----------------------------------------------------------------------------

### Format of Our Data

The data is in the form of a CSV file.

The data is in the form of a table, with each row representing a single record. 
The columns are as follows:

* `Country`: The country the record is from. It is a string. This is a required value
that we joined our data on, and groups the data by country. We will use this to
analyze the data by country.

* `Crop`: The production domain of the record represented as a string. This values
holds the crop that the record is about, either "Maize," "Rice," or "Wheat." This 
is a required value that allows us to group our data by crop. 
We will use this to analyze the data by crop.

* `Year`: The single year the record is from represented as an integer. 
This value ranges from 1990 to 2021. This is a required value that allows us to
group our data by year, and make predictions about the future. Yield ranges
from 

* `Yield`: The yield of the crop in the given country in the given year. 
Measured in tonnes per hectare, it represents the harvested production per unit of harvested area for crop products.

* `Area Harvested`: The area from which the crop is gatered in the given country for the given year.
Measured in hectares, it represents the area of land that is used for crop production.

* `Production`: The total production of the crop in the given country for the given year.
Measured in tonnes, it represents the total domestic production whether inside or outside the agricultural sector, 
i.e. it includes non-commercial production and production from kitchen gardens.

