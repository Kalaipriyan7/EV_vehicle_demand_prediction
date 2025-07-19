# EV_vehicle_demand_prediction
# 🚗 EV Adoption Forecasting with Machine Learning

This project focuses on forecasting electric vehicle (EV) adoption trends across U.S. counties using historical vehicle registration data. It aims to support sustainable infrastructure planning by predicting the future number of EVs.

## 📌 Problem Statement

As electric vehicle adoption increases, urban planners and policymakers must anticipate infrastructure needs like EV charging stations. This project builds a regression model to forecast EV population growth based on historical registration data.

## 📊 Dataset

The dataset is sourced from the [Washington State Department of Licensing](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population-size-2024/data), consisting of **20,819** records with monthly registration details by county.

### Key Columns:
- `Date`: Last day of the month for vehicle counts (e.g., 2020-01-31)
- `County`, `State`: Location of registration
- `Vehicle Primary Use`: `Passenger` or `Truck`
- `Battery Electric Vehicles (BEVs)`
- `Plug-In Hybrid Electric Vehicles (PHEVs)`
- `Electric Vehicle (EV) Total`
- `Non-Electric Vehicle Total`
- `Total Vehicles`
- `Percent Electric Vehicles`

## 🛠️ Tools and Libraries

- **Python 3**
- `pandas`, `numpy` for data handling
- `matplotlib`, `seaborn` for visualization
- `scikit-learn` for preprocessing and modeling
- `joblib` for model persistence

## 🧹 Data Preprocessing

- Converted `Date` to datetime format
- Handled missing values in `County` and `State`
- Detected and capped outliers in `Percent Electric Vehicles`
- Ensured all numeric fields are properly converted
- Removed rows with invalid or null target values

## 🔍 Exploratory Data Analysis (EDA)

- Identified growth trends in EV registrations
- Outlier detection using IQR for `Percent Electric Vehicles`
- Verified completeness and structure of data

## 🤖 Machine Learning Approach

- Model: `RandomForestRegressor`
- Objective: Predict EV Total or Percent EVs based on historical trends
- Data split: `train_test_split`
- Evaluation Metrics:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² Score

## 📈 Forecasting Use Case

The final model can be used to:
- Predict future EV counts for a given county and month
- Estimate future EV infrastructure needs
- Help governments make data-driven policy decisions

## 📁 Project Structure

