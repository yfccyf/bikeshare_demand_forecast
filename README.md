# Bikeshare Demand Forecasting for Efficient Management: Project Overview
* Created a time series model that predictis the next-week bikeshare demand
* Created a prediction tool that predicts the next-day bikeshare demand utilizing weather data and achieved high performance
* Performed thorough feature engineering including categorical variable encoding, numeric variable normalization, feature standardization
* Selected appropriate resampling frequency according to feedback from evaluation metrics
* Built and evaluated regression models inlcuding multiple linear regression, Lasso & Ridge regression, Support Vector Regression, Decision Tree and Random Forest
* Built and evaluated a VAR time series model to perform multivariate time series analysis

## Code and Resources Used
**Python Version:** 3.8
**Packages:** sklearn, statsmodel, datetime, pandas, numpy, scipy, matplotlib, seaborn

## Data Overview
Hourly record of the volume of bikeshare usage and weather data from the end of 2017 to the end of 2018

(After cleaning and processing)

![](images/df_head.png)

## Data Preprocessing
* Combined date and time columns to form a datetime index
* Extracted time parts from datetime column for the convenience of later data visualization
* Resampled data in a lower frequency for later modeling

## EDA
Volume is higher in warmer months, as expected

![](images/monthly.png)

There are 2 peaks during a day - 2 rush hours

![](images/hourly.png)

Volume is highly correlated with average temperture in the long term

![](images/volume_temp.png)

## Feature Engineering
* Adding a constant value to numeric variables
** For the sake of future log transformation, there can't be zero or negative values in the predictor variables
