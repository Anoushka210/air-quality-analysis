# Air Quality EDA and Visualization Project

This project performs Exploratory Data Analysis (EDA) on the **Air Quality in Biggest Cities of the World** dataset from Kaggle.

## Project Overview
This project presents a comprehensive Exploratory Data Analysis (EDA) and visualization of global air quality trends. Using daily pollution records from major cities worldwide, the analysis aims to transform raw environmental data into actionable insights for policy formulation and public health awareness.

The study applies a systematic workflow covering data cleaning, preprocessing, transformation, and advanced visualization techniques to identify patterns in pollutant concentration levels.

## Objectives
- **Pattern Identification:** Identify trends in pollutant concentration levels (PM2.5, PM10, NO₂, SO₂, CO, O₃).
- **Temporal Analysis:** Detect seasonal and temporal variations, specifically highlighting winter month concentrations.
- **Multi-pollutant Assessment:** Analyze relationships between different pollutants across various cities.
- **Advanced Visualization:** Utilize 3D plots to understand spatial and temporal dynamics.
- **Clustering & ML:** Apply K-Means clustering to group cities based on pollutant profiles and perform anomaly detection for extreme events.

## Technologies Used
- **Language:** Python
- **Libraries:**
  - **Data Manipulation:** pandas, numpy
  - **Visualization:** matplotlib, seaborn
  - **Machine Learning:** sklearn

## How to Run
1. Download the dataset from Kaggle: https://www.kaggle.com/datasets/timmofeyy/air-quality-in-biggest-cities-of-the-world
2. Place the CSV file in a folder named `data/` next to the notebook.
3. Open `Air_Quality_EDA_Visualization(Final).ipynb` in Jupyter Notebook (Anaconda).
4. Run all cells sequentially.

## Requirements
- pandas
- numpy
- matplotlib
- seaborn

## Key Insights
**Seasonal Dependency:** Strong correlations found between seasons and pollution levels, with winter months showing significantly higher particulate matter concentrations.

**Regional Characteristics:** Distinct pollution profiles were identified for different regions based on the comparison of gases like NO₂ and O₃ versus Particulate Matter (PM).

**Health Risks:** Analysis of the PM2.5/PM10 ratio highlights specific metropolitan regions with fine-particle dominance, posing higher health risks.
