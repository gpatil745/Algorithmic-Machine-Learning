## **Predicting Taxi Trip Duration in NYC**

## **Overview**

This repository contains the project for predicting taxi trip durations in New York City using exploratory data analysis (EDA), feature engineering, and machine learning models. The goal is to accurately estimate taxi trip durations based on attributes like pickup and drop-off locations, timestamps, and passenger counts.

## **Project Structure**

1. Exploratory Data Analysis and Feature Engineering

Dataset Overview: Historical records of NYC taxi trips with attributes such as pickup/drop-off coordinates, trip duration, passenger count, and timestamps.
Initial Inspection: Loading datasets, examining data types, checking for missing values, and understanding dataset structure.
Data Cleaning: Identifying and correcting inconsistent trip duration values.
Temporal Analysis: Extracting features from timestamps (e.g., day of the week, hour of the day).
Spatial Analysis and Clustering: Visualizing geographical distributions and using MiniBatchKMeans for clustering locations.

2. Model Building

Stacking Ensemble Technique: Combining multiple LightGBM Regressors to improve predictive performance.
Model Architecture: A primary LightGBM Regressor and a meta-model LightGBM Regressor.
Parameter Tuning: Using RandomizedSearchCV for parameter tuning to balance model complexity and generalization.

3. Model Evaluation and Validation

Evaluation Metrics: Mean Squared Logarithmic Error (MSLE) and R-squared.
Generalization and Challenges: Ensuring robust performance on the validation set by handling outliers and fine-tuning hyperparameters.

4. Visualizations

Time Series of Trips: Visualizing the number of trips over time.
Geographical Overlap: Scatter plots showing pickup and drop-off locations.
Distribution of Trip Duration: Histograms of trip durations.
Categorical and Discrete Variables: Count plots of various variables.
Latitude and Longitude Distributions: KDE plots for pickup and drop-off locations.

5. Conclusion and Future Work

Key Findings: Temporal and spatial patterns, along with weather data, were crucial for predictive accuracy.
Future Work: Exploring additional features, experimenting with diverse models, and dynamic hyperparameter tuning.
