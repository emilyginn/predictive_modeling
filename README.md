# Tesla Sales Price Prediction

This project aims to predict the sold prices of Tesla vehicles sold between May 2022 and August 2022 using predictive modeling techniques. The project utilizes machine learning algorithms such as Random Forest, XGBoost, and Gradient Boosting to build predictive models based on historical sales data.

## Table of Contents

- [Overview](#overview)
- [Data](#data)
- [Features](#features)
- [Set Up](#set-up)

## Overview

## Data

## Features

Highlight the key features and functionalities of the project. Include a bullet-point list or brief explanations of the main features implemented in this branch.

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


