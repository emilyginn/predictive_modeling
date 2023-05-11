# Tesla Sales Price Prediction

This project aims to predict the sold prices of Tesla vehicles sold between May 2022 and August 2022 using predictive modeling techniques. The project utilizes machine learning algorithms such as Random Forest, XGBoost, and Gradient Boosting to build predictive models based on historical sales data.

## Table of Contents

- [Set Up](#set-up)
- [Data Preprocessing & Feature Engineering](#data-preprocessing--feature-engineering)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Model Preparation](#model-preparation)
- [Predictive Models](#predictive-models)

## Set Up

The project requires the following libraries to be installed: `boto3`, `pandas`, `numpy`, `scipy`, `matplotlib`, `sklearn`, and `xgboost`.

```python
import boto3
import pandas as pd
import numpy as np
from scipy import stats
import matplotlib.pyplot as plt
from sklearn.preprocessing import LabelEncoder
import xgboost as xgb
from sklearn.ensemble import RandomForestRegressor, GradientBoostingRegressor
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.metrics import mean_absolute_error

## Data Preprocessing & Feature Engineering

The data preprocessing and feature engineering steps include the following:

### Vehicle Specs

- One-hot encoding of the vehicle features in the 'features' column.
- Removal of 'Model S', 'Model X', 'Model 3', 'Model Y' prefixes from trim values.
- One-hot encoding for the trim.
- One-hot encoding for the vehicle model.

### Location

- Extraction of the city from the location column and saving it in title case.
- Removal of rows with missing locations.
- Filling null values for the metro area.

### Date

- Conversion of the date column to days since epoch.

### Location Encoding

- Encoding of the metro and location columns using a LabelEncoder.
- Concatenation of the location and state columns with a hyphen.
- Encoding of the location_state column using a LabelEncoder.

### Calculated Fields

- Calculation of the age of the vehicle in years.
- Calculation of miles per year.
- Calculation of the zScore of the mileage.

### Import Lookup Table

- Importing a lookup table from S3 containing economic indicator data.

## Exploratory Data Analysis

The exploratory data analysis section includes visualizations of the average Tesla model prices by week and the counts of Tesla models sold by week.

## Model Preparation

### Final Feature Selection

- Exclusion of certain columns from the model.

### Splitting the Dataset

- Splitting the dataset into training and test sets.

## Predictive Models

The project uses three predictive models: Random Forest, XGBoost, and Gradient Boosting.

### Random Forest

- Fitting the random forest model.
- Making predictions on the test set.
- Calculating the mean absolute error.

### XGBoost

- Defining the XGBoost model.
- Training the model.
- Predicting on the test set.
- Calculating the mean absolute error.

### Gradient Boost

- Creating the Gradient Boosting model.
- Fitting the model to the training data.
- Predicting on the test set.
- Calculating the mean absolute error.

The mean absolute error (MAE) is calculated for each model as a measure of prediction accuracy.
