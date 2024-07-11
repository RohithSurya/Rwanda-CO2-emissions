# Predicting CO2 Emissions in Rwanda

This project is a part of CS-4661 at Calstate LA and taught by [Mohammad Pourhomayoun](https://www.calstatela.edu/faculty/mohammad-pourhomayoun)


The project is to create machine learning models that use open-source emissions data (from Sentinel-5P satellite observations) to predict carbon emissions.

Kaggle Dataset Link: https://www.kaggle.com/competitions/playground-series-s3e20

Approximately 497 unique locations were selected from multiple areas in Rwanda, with a distribution around farm lands, cities and power plants. The data for this competition is split by time; the years 2019 - 2021 are included in the training data, and your task is to predict the CO2 emissions data for 2022 through November.

Seven main features were extracted weekly from Sentinel-5P from January 2019 to November 2022. Each feature (Sulphur Dioxide, Carbon Monoxide, etc) contain sub features such as column_number_density which is the vertical column density at ground level, calculated using the DOAS technique.

Sulphur Dioxide - COPERNICUS/S5P/NRTI/L3_SO2  
Carbon Monoxide - COPERNICUS/S5P/NRTI/L3_CO  
Nitrogen Dioxide - COPERNICUS/S5P/NRTI/L3_NO2  
Formaldehyde - COPERNICUS/S5P/NRTI/L3_HCHO  
UV Aerosol Index - COPERNICUS/S5P/NRTI/L3_AER_AI  
Ozone - COPERNICUS/S5P/NRTI/L3_O3  
Cloud - COPERNICUS/S5P/OFFL/L3_CLOUD  

## Conclusion
- We used data visualization tools to look for patterns and anomalies in the data. We found that the data during the COVID-19 pandemic is an anomaly as most of the world slowed down, so it resulted in reduced CO2 emissions. For this reason, we removed the CO2 data during the COVID-19 time frame.
- The data plots and visualization also ensured that some of the features were irrelevant to the task. So, we removed those features, reducing our search space and noise.
- We finally used [DecisionTreeRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html) and [RadiusNeighborsRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.RadiusNeighborsRegressor.html) to predict the CO2 emission.
- After that, we plotted the model prediction using visualization plots. 