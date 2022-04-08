# Project Goal
Using 2017 properties and prediction data from our Zillow database for single unit/single family homes, we were tasking with improving the log error (Zestimate). We will be using the ML Clustering Algorithm KMeans to find clusters within the data to improve our estimate of the log error.I will create Regression models to predict logerror and find the key drivers. One step further, hope this study can improve our understanding to log error, and provide useful information for future study. 
***

# Project Description

Zillow has data on roughly 110 million homes across the United States.The company offers several features, including value estimates of homes, value changes of each home in a given time frame, aerial views of homes, and prices of comparable homes in the area. It also provides basic information on a given home, such as square footage and the number of bedrooms and bathrooms. Users can also get estimates of homes that have undergone significant changes, such as a remodeled kitchen.

As the most visited real estate website in the United States, Zillow and its affiliates provide customers with an on-demand experience selling, buying, leasing and financing with a transparent and near-seamless end-to-end service. However, as we all know, the real estate market is constantly volatile and changing. 

Zillow's Zestimate is an estimate of value using a proprietary formula created by the online real estate database company. Zestimates cover more than 100 million homes across the United States. A Zestimate is calculated from physical attributes, tax records, and user submitted data. 
***

# Project Planning
Plan -> Acquire -> Prepare -> Explore -> Model & Evaluate -> Deliver
Planning:

***Create a README file (check!)***
* Ensure my dataprep.py modules are well documents and functional

***Acquisition***

* Obtain Zillow data from Codeup mySQL database via dataprep.py

***Preparation***

* Clean Zillow data from Codeup mySQL database via wrangldataprepe.py


***Exploration and Pre-processing***

* Ask and answer statistical questions about the Zillow data
* Visually represent findings with charts

***Exploration and Clustering***
* Clustering Algorithm KMeans to find clusters within the data to improve our estimate of the log error.

***Modeling***

* Split data appropriately
* Use knowledge acquired from statistical questions to help choose a model
* Create a predictions csv file from the best model

***Deliver***

* Deliver a 5 minute presentation via a jupyter notebook walkthrough
* Answer questions about my code, process, and findings

***
# Data Dictionary
* yearbuilt: The Year the principal residence was built
* fips: Federal Information Processing Standard code
* calculatedfinishedsquarefeet: Calculated total finished living area of the home
* bathroomcnt: Number of bathrooms in home including fractional bathrooms
* bedroomcnt: Number of bedrooms in home
* taxvaluedollarcnt: The total property tax assessed for that assessment year
* latitude: Latitude of the middle of the parcel multiplied by 10e6
* longitude: Longitude of the middle of the parcel multiplied by 10e6
* lotsizesquarefeet: Area of the lot in square feet
* propertylandusetypeid:  Type of land use the property is zoned for
* regionidcounty:County in which the property is located
* regionidcity: City in which the property is located (if any)
* regionidzip:Zip code in which the property is located
* regionidneighborhood:	Neighborhood in which the property is located
* roomcnt: Total number of rooms in the principal residence
* assessmentyear: The year of the property tax assessment 
***
# Steps to Reproduce
You will need your own env file with database credentials along with all the necessary files listed below to run the "Final Report" notebook.

Read this README.md

Download at the aquire.py and Final Report.ipynb file into your working directory

Create a .gitignore for your .env file

Add your own env file to your directory with username, password, and host address.

Import Basemap package. 

Run the final_report.ipynb notebook

***
# Initial Questions:


What's the distribution of the logerror? 

What are the correlation coefficients between variables? 

What areas are we focusing on?

Does year built impact logerror?

Does bedroom count impact logerror?

Does bathroom count impact logerror?

***

# Model
Select a metric to use for evaluating models and explain why that metric was chosen.
Create and evaluate a baseline model.
Find mean value of target
Set all predictions to that value
Evaluate based on selected evaluation metric
Develop Four models.
Evaluate all four models on the train sample, note observations.
Evaluate the top performing model on the test sample, note observations.

***
# Key Findings
There is a relationship between tax_value, area, and bedroom count in predicting the logerror of single family units. Bedrooms and tax value cluster also were shown as useful. 

I didn't find any feature that strongly correlate with log error. 
*** 
# Recomandation
We can continue using the existing model to predict the logerror. The data suggest bedrooms, and area and tax_values to be the most valued features. I recommend removing outliers from these columns to improve future modeling.

# Next Steps 
With more time I would work on improving the model adding more parameters

With more time, I would like to dive deeper into the zillow database and implement feature engineering to discover the best combination of available features to predict home values.