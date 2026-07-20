# 🌱 Agricultural Yield Prediction in West Africa Using Climate and Agricultural Data

## 📌 Project Overview

This project focuses on predicting agricultural yield in West Africa by combining historical agricultural data with climate information.

The objective is to understand how environmental conditions and agricultural factors influence crop productivity and to prepare a dataset for machine learning prediction.

This project combines:

- 🌾 Agricultural data from FAOSTAT
- ☁️ Climate data from NASA POWER API
- 🌍 Geographic information

---

## 🎯 Project Objectives

The main goals of this project are:

- Analyze agricultural productivity trends in West Africa
- Study the relationship between climate variables and crop yields
- Combine multiple real-world datasets
- Clean and prepare data for machine learning
- Predict crop yield using data-driven approaches

---

# 📊 Dataset Overview

Two datasets were used:

## 🌾 FAOSTAT Agricultural Dataset

Source: Food and Agriculture Organization of the United Nations (FAOSTAT)

The dataset contains:

- Country
- Year
- Crop
- Production
- Harvested area
- Yield (kg/ha)

The project focuses on **16 West African countries**:

- Benin
- Burkina Faso
- Cabo Verde
- Côte d'Ivoire
- Gambia
- Ghana
- Guinea
- Guinea-Bissau
- Liberia
- Mali
- Mauritania
- Niger
- Nigeria
- Senegal
- Sierra Leone
- Togo

---

## ☁️ NASA POWER Climate Dataset

Source: NASA POWER API

Climate variables collected:

- Average temperature
- Maximum temperature
- Minimum temperature
- Precipitation
- Relative humidity
- Solar radiation
- Wind speed
- Soil temperature

The climate data was collected using country geographic coordinates.

---

# 🎯 Target Variable

The prediction target is:

**Yield (kg/ha)**

Yield represents agricultural productivity by measuring the amount of crop production obtained per hectare.

---

# 🧹 Data Preprocessing

Data preparation steps included:

- Removing unnecessary columns
- Handling missing values
- Converting data types
- Cleaning unreliable observations
- Reshaping climate data
- Merging FAOSTAT and NASA POWER datasets

The final dataset combines:

- Crop information
- Historical yield
- Climate conditions
- Geographic information

---

# 📈 Exploratory Data Analysis

The analysis explored:

- Yield distribution by crop
- Yield comparison between countries
- Agricultural productivity evolution over time
- Relationship between climate conditions and crop production

---

# 🛠️ Technologies Used

## Programming

- Python

## Data Analysis

- Pandas
- NumPy

## Visualization

- Matplotlib
- Seaborn

## Machine Learning

- Scikit-learn

## Environment

- Jupyter Notebook

---

👩🏽‍💻 Author

**Grace Diagoné**

Data Analytics / Data Science Student
