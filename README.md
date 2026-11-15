# Retail Store Item Demand Forecasting

A time-series machine learning project that forecasts daily product demand across multiple retail stores using historical sales data, engineered temporal features and LightGBM.

## Problem Statement

Retailers need reliable demand estimates to support inventory planning, replenishment and stock allocation. This project studies historical sales patterns and builds a model to predict demand for individual store-product combinations.

## Dataset

[Store Item Demand Forecasting — Kaggle](https://www.kaggle.com/competitions/demand-forecasting-kernels-only)

- Historical period: January 2013 – December 2017
- Stores: 10
- Products: 50
- Store-product combinations: 500
- Forecast horizon: 3 months

## Methodology

1. **Exploratory Data Analysis:** Examined sales distributions, trends, store/product differences and seasonality.
2. **Time-Series Analysis:** Investigated temporal patterns and seasonal behaviour.
3. **Feature Engineering:** Created calendar, lag, rolling-statistic and exponentially weighted features.
4. **Feature Selection:** Used Recursive Feature Elimination (RFE).
5. **Model Development:** Trained a LightGBM regression model.
6. **Hyperparameter Optimization:** Used Optuna.
7. **Evaluation:** Used chronological validation and time-series cross-validation.
8. **Interpretability:** Used feature importance and SHAP analysis.

## Model Performance

| Metric | Test Result |
|---|---:|
| MAE | 6.10 |
| MAPE | 13.29% |
| RMSE | 7.97 |
| R² | 0.9221 |

These values are taken from the saved evaluation output in the modelling notebook.

## Technology Stack

- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn, LightGBM
- Statsmodels
- Optuna
- SHAP
- Jupyter Notebook

## Project Structure

```text
store-item-demand-forecasting/
├── input/
├── models/
├── notebooks/
├── reports/
├── src/
├── requirements.txt
├── setup.py
└── README.md
```

## Installation

```bash
git clone https://github.com/jayant13042004/store-item-demand-forecasting.git

cd store-item-demand-forecasting

python -m venv .venv

# Windows
.venv\Scripts\activate

pip install -r requirements.txt
```

Open the notebooks directory and execute the notebooks in their intended order. Ensure the required dataset files are available in the expected input location.

## Potential Applications

- Store-level inventory planning
- Product-level replenishment
- Seasonal demand planning
- Identifying high- and low-demand products

## Acknowledgements

Dataset: [Kaggle Store Item Demand Forecasting Challenge](https://www.kaggle.com/competitions/demand-forecasting-kernels-only).

Implementation reference: [allmeidaapedro/Store-Item-Demand-Forecasting](https://github.com/allmeidaapedro/Store-Item-Demand-Forecasting).

## Author

**Jayant Jagtap**

[GitHub](https://github.com/jayant13042004)
