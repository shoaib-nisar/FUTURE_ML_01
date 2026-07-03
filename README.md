# Sales & Demand Forecasting for Businesses

## Overview
A time series forecasting model that predicts future monthly 
sales for the Superstore retail dataset using SARIMA.

## Dataset
Superstore Sales Dataset — 9,994 orders from 2014 to 2017
Source: https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

## Approach
- Cleaned and aggregated raw order data to monthly time series
- Explored trend and seasonality via decomposition
- Confirmed non-stationarity with ADF test
- Selected SARIMA parameters using ACF/PACF plots
- Trained SARIMA(1,1,0)(1,1,0,12) on 42 months
- Evaluated on 6-month holdout test set

## Results
| Metric | Value |
|--------|-------|
| MAE    | $14,727 |
| RMSE   | $16,990 |
| MAPE   | 17.5%   |
| Naive Baseline MAPE | 25.4% |
| Beats Naive | ✅ Yes, by 8.0% |

## Forecast
Model predicts next 12 months of sales with 95% 
confidence intervals. Peak month and slowest month 
identified for inventory and staffing planning.

## Business Insight
- Total forecasted revenue: $X (fill in your number)
- Peak month: (fill in)
- Recommended: increase inventory before peak month,
  reduce orders in slowest month

## Files
- `sales_forecasting.ipynb` — full notebook
- `Sample - Superstore.csv` — dataset (or link to Kaggle)

## Libraries Used
pandas, numpy, matplotlib, seaborn, statsmodels, sklearn
