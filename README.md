# Stock Price Time Series Analysis (AAPL)

Time series analysis of Apple (AAPL) daily closing prices, 2018 to 2026.

## Objective
Analyze time-based patterns in stock prices:
- Trend analysis
- Seasonality detection
- Forecasting future values (optional)

## Dataset
Daily closing prices downloaded from Yahoo Finance using the `yfinance` library (adjusted for splits and dividends).

## Tools Used
Python, pandas, NumPy, Matplotlib, statsmodels, yfinance

## Methods
1. **Trend:** 50-day and 200-day moving averages
2. **Seasonality:** seasonal decomposition (multiplicative, 12-month period) and average return by calendar month
3. **Forecast:** ARIMA(1,1,1) model on log prices, predicting the next 30 business days

## Key Findings
| Insight | Result |
|---|---|
| Overall trend | Strong upward: $40.23 to $338.83 (+742%) |
| Trend signal | Price stays above the 200-day moving average |
| Seasonality | Clear yearly pattern, about +/-5% around the trend |
| Strongest months | July (+7.4%), August (+6.1%) |
| Weakest months | September (-1.5%), February (-1.0%) |
| 30-day forecast | $338.31 (95% range: $278.87 to $410.40) |

## How to Run
1. Open `Untitled2.ipynb` in [Google Colab](https://colab.research.google.com) or Jupyter.
2. Click **Runtime > Run all**.
3. To analyze another stock, change `"AAPL"` in the first cell (for example `"TCS.NS"`).

## Limitations
- Monthly seasonal averages are based on about 8 to 9 years of data, so they are tendencies, not guarantees.
- Stock prices are close to a random walk, so the forecast is only an estimate and uncertainty grows over longer horizons.
- This project is for learning purposes and is not financial advice.
