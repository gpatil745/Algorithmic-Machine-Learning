# **Predicting Taxi Trip Duration in NYC**
Welcome to the GitHub repository for my project on predicting taxi trip durations in New York City. This project is part of my coursework at Rutgers Business School, where I am pursuing a Master's in Information Technology and Analytics. Below is an overview of the project, including the exploratory data analysis (EDA), feature engineering, model building, and evaluation processes.

## **Project Overview**
This project aims to predict the duration of taxi trips in New York City using historical trip data. The dataset includes attributes such as pickup and drop-off coordinates, trip duration, passenger count, and timestamps. The objective is to build a predictive model that can accurately forecast trip durations based on these features.

## **Exploratory Data Analysis (EDA)**
### Initial Data Inspection
The project begins with loading the datasets into Pandas DataFrames, followed by an initial exploration to understand the data structure. This step involves checking data types, identifying missing values, and gaining a high-level overview of the dataset.

### Data Cleaning
Inconsistent trip durations were identified by comparing calculated durations from timestamps with provided trip durations. Discrepancies were corrected to ensure data consistency.

### Temporal and Spatial Analysis
Temporal patterns were analyzed by extracting features from timestamps, such as the day of the week and hour of the day. Spatial analysis involved visualizing pickup and drop-off locations, and clustering these locations using MiniBatchKMeans to create meaningful features for the predictive model.

### Feature Engineering
Key features such as distance between pickup and drop-off points, trip duration outliers, and weather data were engineered to enhance the model's predictive power. This comprehensive feature engineering process aimed to capture relevant temporal and spatial patterns in the data.

## **Model Building**
A stacking ensemble technique was chosen to leverage the strengths of multiple models. Two LightGBM Regressors were used: one as the primary model and the other as a meta-model. The meta-model was trained on the predictions of the primary model combined with the original features. Extensive parameter tuning was performed to optimize model performance.

## **Model Evaluation**
The model's performance was evaluated using Mean Squared Logarithmic Error (MSLE) and R-squared metrics. The model demonstrated strong generalization on the validation set, with competitive scores. Challenges such as handling outliers and fine-tuning hyperparameters were addressed through robust preprocessing and careful parameter tuning.

## **Visualizations**
The project includes various visualizations to illustrate the analysis and modeling steps:

- Time series of trips
- Geographical overlap of pickups and drop-offs
- Distribution of trip durations
- Distributions of categorical and discrete variables
- Latitude and longitude distributions

## **Conclusion and Future Work**
The project successfully developed a robust predictive model for taxi trip durations in NYC. Key findings include the importance of temporal and spatial features and the effectiveness of the stacking ensemble technique. Future work could focus on further feature engineering, experimenting with a broader range of base models, and implementing dynamic hyperparameter tuning.
