🌱 Agricultural Yield Prediction in West Africa Using Climate and Agricultural Data
📌 Project Overview

This project focuses on developing a data-driven agricultural yield prediction system by combining historical crop production data with climate information.

The project was developed for Verdant Analytics, an agri-tech consultancy that builds data solutions for food producers, commodity traders, and food security organizations.

The client, GlobalGrain Foods, purchases staple crops several months before harvest. Therefore, accurate yield forecasting is essential to anticipate:

🌾 Supply shortages
💰 Increased procurement costs
🚚 Production and distribution disruptions

Currently, agricultural decisions rely mainly on expert reports and regional estimations, which can be delayed and inconsistent.

This project explores how agricultural statistics and climate data can be combined to build predictive insights for crop yield forecasting.

🎯 Project Objective

The main objective is to predict agricultural yield using:

Historical crop production data
Climate and environmental variables
Geographic information

The project aims to:

Analyze agricultural productivity trends in West Africa
Understand the relationship between climate conditions and crop yields
Combine multiple real-world datasets
Prepare a machine learning-ready dataset
Develop a predictive model for crop yield estimation
📊 Dataset Overview

Two main datasets were combined:

FAOSTAT Agricultural Data
NASA POWER Climate Data

The final dataset combines:

🌱 Agricultural information
+
🌦 Environmental conditions

to explain variations in crop productivity.

1. 🌾 FAOSTAT Agricultural Dataset
Source

Food and Agriculture Organization of the United Nations (FAOSTAT)

FAOSTAT provides historical agricultural statistics:

Crop production
Harvested area
Yield
Country
Year
Crop category
Why FAOSTAT?

FAOSTAT was selected because it provides:

Long historical records
International agricultural data
Crop-level information
Reliable statistics from multiple countries
🌍 Geographic Scope

The project focuses on 16 West African countries.

Countries included:

Benin
Burkina Faso
Cabo Verde
Côte d'Ivoire
Gambia
Ghana
Guinea
Guinea-Bissau
Liberia
Mali
Mauritania
Niger
Nigeria
Senegal
Sierra Leone
Togo

The objective was to compare agricultural productivity between countries and evaluate how climate variability affects different regions.

🌱 Selected Crops

The dataset includes several agricultural categories:

Cereals
Maize
Rice
Sorghum
Millet
Fonio
Roots & Tubers
Cassava
Yams
Sweet potatoes
Legumes
Cow peas
Groundnuts
Fruits & Vegetables
Plantains
Tomatoes
Okra
Cash Crops
Cocoa beans
Cotton
Sugar cane
Palm oil
Tree Crops
Coconut
🎯 Target Variable

The prediction target is:

Yield (kg/ha)

Yield represents:

The amount of agricultural production obtained per hectare of cultivated land.

It was selected because it directly measures agricultural productivity.

📅 Time Period

FAOSTAT historical data:

1961 - 2024

This long period allows analysis of:

Agricultural evolution
Productivity changes
Long-term climate impacts
2. ☁️ NASA POWER Climate Dataset
Source

NASA POWER API

NASA POWER provides satellite-based climate and environmental observations.

The dataset was used to capture climate conditions influencing crop growth.

🌍 Geographic Coordinates

NASA POWER requires latitude and longitude coordinates.

Each country was associated with a geographic centroid:

Example:

Country	Latitude	Longitude
Côte d'Ivoire	7.5400	-5.5471
Ghana	7.9465	-1.0232
Nigeria	9.0820	8.6753

These coordinates were used to retrieve climate information through the API.

🌦 Climate Variables Selected

The selected variables represent the main factors influencing agricultural production.

Variable	Description
T2M	Average temperature
T2M_MAX	Maximum temperature
T2M_MIN	Minimum temperature
RH2M	Relative humidity
PRECTOTCORR	Precipitation
ALLSKY_SFC_PAR_TOT	Solar radiation available for photosynthesis
WS2M	Wind speed at 2 meters
WS10M	Wind speed at 10 meters
TS	Soil surface temperature
T2MDEW	Dew point temperature
T2MWET	Wet bulb temperature

These variables cover:

🌡 Temperature
💧 Water availability
☀️ Solar radiation
🌱 Soil conditions
🌬 Wind
💦 Humidity
🔄 Data Collection Pipeline

NASA POWER data was collected automatically using the API.

The extraction process:

Load country coordinates
Send requests to NASA POWER API
Retrieve yearly climate observations
Store results
Combine all countries into one dataset

The API process only retrieves information.

No climate values were calculated manually.

🧹 Data Preprocessing

Before modeling, both datasets were cleaned and prepared.

FAOSTAT Cleaning

Performed steps:

Removed unnecessary administrative columns
Checked missing values
Converted data types
Removed unreliable observations
Defined Yield as target variable

Removed columns:

Column	Reason
Domain Code	Technical identifier
Area Code	Country identifier
Item Code	Crop identifier
Unit	Not needed after selecting Yield
NASA POWER Cleaning

Performed steps:

Inspected dataset structure
Checked missing values
Converted data types
Removed irrelevant variables

NASA POWER missing values:

-999

were replaced by:

NaN

to avoid incorrect calculations.

🔄 NASA POWER Reshaping

Original format:

Country	Year	Parameter	Value
Côte d'Ivoire	2020	T2M	26
Côte d'Ivoire	2020	RH2M	75

Converted format:

Country	Year	T2M	RH2M
Côte d'Ivoire	2020	26	75

Final structure:

One row = One Country + One Year
🔗 Dataset Integration

The two datasets were merged using:

Country + Year

Final feature table:

Country	Year	Crop	Yield	Temperature	Rainfall	Humidity
Côte d'Ivoire	2020	Cocoa	xxx	xx	xx	xx

The final dataset contains:

Crop information
Historical yield
Climate conditions
Geographic information
📈 Exploratory Data Analysis

After merging the datasets, exploratory analysis was performed.

The analysis focused on:

🌱 Yield Distribution by Crop

Objectives:

Compare productivity between crops
Understand yield variability
🌍 Yield Distribution by Country

Objectives:

Compare agricultural performance between countries
Identify regional differences
 Yield Evolution Over Time

Questions:

How has crop productivity changed between 1963 and 2023?
Which countries experienced productivity improvement or decline?
🛠️ Technologies Used
Programming
Python
Data Analysis
Pandas
NumPy
Visualization
Matplotlib
Seaborn
Machine Learning
Scikit-learn
Environment
Jupyter Notebook

 Project Structure
Agricultural-Yield-Prediction/

│
├── data/
│   ├── FAOSTAT.csv
│   └── NASA_POWER.csv
│
├── notebooks/
│   └── Agricultural_Yield_Predictor.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt


👩🏽‍💻 Author

Grace Diagoné

Data Analytics / Data Science Student
