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
