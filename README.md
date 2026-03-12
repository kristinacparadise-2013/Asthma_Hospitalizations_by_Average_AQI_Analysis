# Asthma_Hospitalizations_by_Average_AQI_Analysis
Does AQI affect asthma hospitalizations?

This project investigates the relationship between air quality and asthma hospitalization rates across U.S. counties from 2021 to 2023. It combines public health data with environmental exposure data to perform a biostatistical analysis using SQL for data integration and Python for cleaning, analysis, and visualization.

The goal is to determine whether higher levels of air pollution are associated with increased asthma hospitalizations.
Question:
Is poorer air quality (higher AQI) associated with higher asthma hospitalization rates at the county level in the U.S. between 2021–2023?

Data Sources:
Asthma Hospitalizations
Source: Centers for Disease Control and Prevention (CDC) Environmental Public Health Tracking Network
Data: County-level asthma hospitalization rates, 2021–2023

Air Quality Index (AQI)
Source: U.S. Environmental Protection Agency (EPA) Air Quality System
Data: County-level AQI values for 2021–2023

All datasets are publicly available and were downloaded as CSV files.

Project Workflow:

Data Integration (SQL)
Multiple yearly AQI tables were combined using UNION ALL.
Asthma data and AQI data were joined using JOIN statements on state, county, and year.
Aggregation (GROUP BY) was used to calculate average AQI and hospitalization rates at the county-year level.

Data Cleaning (Python)
Handled missing values and ensured numerical types for analysis.
Verified consistency of county and state names between datasets.

Statistical Analysis (Python)
Pearson correlation test to measure the association between average AQI and asthma hospitalization rates.
Linear regression to visualize the relationship.

Visualization (Python)
Scatter plots with regression line to illustrate correlation.

Key Findings:
The correlation between average AQI and asthma hospitalization rates is very weak (r = 0.045).
The p-value of 0.084 indicates that the relationship is not statistically significant at the 0.05 level.
The regression line in the scatter plot is nearly flat, suggesting little to no linear relationship between AQI and asthma hospitalizations in this dataset.

Interpretation:
Average AQI alone does not appear to be a strong predictor of asthma hospitalization rates across U.S. counties for the years analyzed. Other factors, such as population demographics, healthcare access, and specific pollutants (e.g., PM2.5, ozone), may have more influence on hospitalization risk.

Limitations:
AQI is a combined measure of multiple pollutants and may mask effects of specific pollutants linked to asthma.
Hospitalization rates are influenced by healthcare access, population density, and reporting practices.
Analysis is limited to 2021–2023, so longer-term trends are not assessed.

Clear labels and titles to communicate findings effectively.
