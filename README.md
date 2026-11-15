
# Retail Demand Forecasting & Predictive Analytics

An end-to-end machine learning project for forecasting retail product demand across multiple stores using historical sales data, time-series analysis, and gradient boosting.

## Project Overview

Accurate demand forecasting is essential for retail businesses to optimize inventory, reduce stockouts, minimize overstocking, and improve supply-chain planning.

This project analyzes historical sales data from 10 stores and 50 products to identify demand patterns and forecast future sales over a three-month horizon.

The solution uses time-series feature engineering and machine learning to capture trends, seasonality, and store-product-specific sales behavior.

## Business Objectives

- Forecast product-level demand across multiple retail stores.
- Identify seasonal trends and recurring sales patterns.
- Understand variations in demand across stores and products.
- Improve inventory planning through data-driven predictions.
- Translate model predictions into actionable business insights.

## Dataset

**Store Item Demand Forecasting Dataset**

- Historical period: January 2013 – December 2017
- Number of stores: 10
- Number of products: 50
- Store-product combinations: 500
- Forecast horizon: 3 months

Dataset: [Kaggle – Store Item Demand Forecasting Challenge](https://www.kaggle.com/competitions/demand-forecasting-kernels-only)

## Technology Stack

- **Programming:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn, LightGBM
- **Time-Series Analysis:** Statsmodels
- **Hyperparameter Optimization:** Optuna
- **Model Interpretability:** SHAP
- **Development:** Jupyter Notebook, Git

## Methodology

### 1. Exploratory Data Analysis
- Analyzed historical sales trends and distributions.
- Identified weekly and yearly seasonality.
- Examined demand variations across stores and products.
- Investigated trends, outliers, and demand patterns.

### 2. Time-Series Analysis
- Decomposed sales into trend, seasonal, and residual components.
- Analyzed stationarity and temporal dependencies.
- Identified relevant forecasting patterns.

### 3. Feature Engineering
Developed predictive features including:

- Calendar features: day, month, year, weekday, and day of year.
- Lag features: historical sales at different time intervals.
- Rolling statistics: moving averages and standard deviations.
- Exponentially weighted moving averages.
- Store and product identifiers.

### 4. Model Development
Implemented a LightGBM regression-based forecasting approach to capture nonlinear relationships between historical sales patterns and future demand.

Model development includes:
- Baseline model comparison.
- Feature selection using Recursive Feature Elimination.
- Hyperparameter optimization using Optuna.
- Chronological training and validation.

### 5. Model Evaluation
Evaluated forecasting performance using:

- Mean Absolute Error (MAE)
- Mean Absolute Percentage Error (MAPE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

Also analyzed residual distributions and actual-versus-predicted sales.

### 6. Model Interpretability
Used feature importance and SHAP analysis to understand the contribution of historical sales, calendar variables, and rolling statistics to demand predictions.

### 7. Business Insights
The forecasting outputs can support:

- Store-level inventory planning.
- Product-level replenishment decisions.
- Identification of high-demand and low-demand products.
- Seasonal demand planning.
- Sales and inventory allocation.

## Project Structure

```text
├── input/
├── models/
├── notebooks/
├── reports/
├── src/
├── requirements.txt
├── setup.py
└── README.md
```

## Installation & Execution

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_NAME>

python -m venv venv

# Windows
venv\Scripts\activate

pip install -r requirements.txt

jupyter notebook
```

Open the notebooks directory and execute the exploratory analysis and modeling notebooks.

## Future Improvements

- Compare LightGBM against XGBoost, Prophet, and ARIMA.
- Develop LSTM-based forecasting models.
- Build an interactive demand forecasting dashboard.
- Integrate automated forecasting pipelines.
- Extend predictions into inventory optimization and replenishment planning.

## Acknowledgements

This project is based on the Store Item Demand Forecasting Challenge hosted on Kaggle.

Original project inspiration and implementation reference:
https://github.com/allmeidaapedro/Store-Item-Demand-Forecasting

Dataset:
https://www.kaggle.com/competitions/demand-forecasting-kernels-only
