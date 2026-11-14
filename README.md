# Retail Demand Forecasting

Forecasting daily item-level demand for a retail chain, benchmarked against naive baselines, with seasonality analysis.

> Fill every [bracket] from your own run. Do not publish numbers you did not produce.

## Dataset
Kaggle "Store Item Demand Forecasting Challenge": 10 stores × 50 items, daily sales, 2013-01-01 to 2017-12-31.

## Approach
1. **EDA:** weekly and yearly seasonality, trend, store/item differences
2. **Validation:** chronological split; last [90] days held out as test; `TimeSeriesSplit` for tuning
3. **Baselines:** naive and seasonal-naive (weekly)
4. **Models:** [SARIMA / Prophet] and LightGBM with lag, rolling-window, and calendar features
5. **Metrics:** WAPE, MAPE (excluding zero-sales days), RMSE
6. **Inventory planning (only if built):** reorder point and safety stock from forecast error
7. **App (only if built):** Streamlit page for forecast vs actual by store and item

## Results (test period)
| Model | WAPE | MAPE | RMSE |
|---|---|---|---|
| Naive | [x] | [x] | [x] |
| Seasonal-naive | [x] | [x] | [x] |
| [SARIMA/Prophet] | [x] | [x] | [x] |
| **LightGBM** | **[x]** | **[x]** | **[x]** |

LightGBM improves WAPE by [y]% over seasonal-naive.
(Add a forecast-vs-actual plot: `![forecast](images/forecast.png)`)

## Run locally
```bash
git clone https://github.com/jayant13042004/store-item-demand-forecasting.git
cd store-item-demand-forecasting
pip install -r requirements.txt
jupyter notebook notebooks/[notebook].ipynb
```

## Limitations
- One holdout window; no rolling-origin evaluation across periods.
- Point forecasts only; no prediction intervals.

## References
List any repositories or tutorials you took ideas from, with links.

## Author
Jayant Jagtap · [LinkedIn](https://www.linkedin.com/in/jayantjagtap/)
