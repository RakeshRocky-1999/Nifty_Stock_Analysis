# NiftyScope: Time Series Forecasting of Nifty 50 Stocks

## 📊 Overview
This project performs end-to-end time series analysis and forecasting on historical stock prices of Nifty 50 companies. We explore traditional statistical models like **ARIMA**, **SARIMAX**, and advanced deep learning models like **LSTM** to predict stock prices for the next 90 business days.

The project provides insights into market trends, stock performance, and forecasting accuracy — helping build better investment strategies.

---

## 🧠 Objectives
- Perform Exploratory Data Analysis (EDA) on Nifty 50 stocks.
- Apply multiple forecasting models: ARIMA, SARIMAX, and LSTM.
- Compare model performance and prediction trends.
- Visualize actual vs predicted prices for each stock.
- Forecast future price trends for better decision-making.

---

## 📂 Dataset
- **Source**: [Kaggle - Nifty50 Stock Market Data](https://www.kaggle.com/datasets/rohanrao/nifty50-stock-market-data)
- **Period**: ~2000 to 2021
- **Stocks**: Nifty 50 companies
- **Features**: `Date`, `Symbol`, `Open`, `High`, `Low`, `Close`, `Volume`

---

## 🔍 Exploratory Data Analysis
- Line plots of stock price trends (Close) over time.
- Volume analysis and trading patterns.
- Summary statistics and volatility measures.
- Identification of top/bottom performing stocks.
- Stationarity check using ADF test (for ARIMA-based models).

---

## ⚙️ Models Used

### 🔢 ARIMA
- Applied on individual stock closing prices.
- Differencing to remove trend & seasonality.
- AIC and PACF/ACF plots for parameter selection.
- Short-term forecasting.

### 📈 SARIMAX
- Seasonal ARIMA model with exogenous variables (e.g., volume).
- Captures both trend and seasonality more effectively.
- Grid search for optimal `(p,d,q)(P,D,Q)s` values.
- Medium-term prediction accuracy improvement over ARIMA.

### 🤖 LSTM (Long Short-Term Memory)
- Deep learning model for time series forecasting.
- Uses sliding windows (last 60 days) to predict next value.
- 2-layer LSTM with dropout and dense output layer.
- Recursive forecasting for 90 business days into the future.

---

## 🔄 Forecasting Strategy
- All models trained per stock individually.
- LSTM forecasting handled future business days using last known sequence.
- Plots include:
  - Actual prices from 2021
  - Predicted prices for next 90 days

---

## 📊 Visualizations
- Line charts showing:
  - Historical stock prices
  - ARIMA/SARIMAX/LSTM predicted prices
  - Comparison across models
- Focused only on latest period (2021 + Forecast)
- Annotated charts with trends, patterns, and model names

---

## 📌 Insights Extracted
- **ARIMA** works well on stationary stocks, but struggles with high volatility.
- **SARIMAX** performs better where seasonal patterns are present.
- **LSTM** handles long-term non-linear trends and outperforms on smoothly trending stocks.
- Forecasts revealed potential outperformers in 2021 (e.g., ASIANPAINT, INFY, TCS).
- Traditional models are faster to train; LSTM more accurate in longer horizons.

---

## 📦 Tools & Technologies
- Python
- Pandas, NumPy, Matplotlib, Seaborn
- Statsmodels (ARIMA, SARIMAX)
- Scikit-learn
- TensorFlow/Keras (LSTM)
- Jupyter Notebook

---

## 🚀 Future Enhancements
- Add model performance metrics (MAE, RMSE) for each stock and model.
- Ensemble forecasting (average of all models).
- Build a portfolio optimization strategy based on LSTM output.
- Deploy with Streamlit or Flask for real-time use.

---

## 👤 Author
- **Rakesh B**
- [GitHub](https://github.com/RakeshRocky-1999) | [LinkedIn](https://www.linkedin.com/in/rakesh-b-9b7709290/)

