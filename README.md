# 📈 Stock Price Prediction with LSTM

## Overview
This project explores stock price modeling for **AMD (Advanced Micro Devices)** using a deep learning approach based on **LSTM (Long Short-Term Memory)** networks.

Unlike naive price prediction models, this implementation incorporates **Shannon Entropy** as a feature to quantify market uncertainty, alongside traditional price-based features.

The goal is not just prediction, but understanding how **information randomness affects time-series learning**.

---

## Key Idea
Most basic models rely only on price history.

This project combines:
- **Temporal structure** → captured by LSTM  
- **Market uncertainty** → captured by entropy  

This creates a richer representation of financial time series.

---

## Features Used
- Closing Price  
- Log Returns  
- Rolling Shannon Entropy  

---

## Methodology

### 1. Data Collection
- Source: Yahoo Finance (`yfinance`)
- Asset: AMD stock
- Time range: 2018–2024

### 2. Feature Engineering
- Log returns: $r_t = \log\left(\frac{P_t}{P_{t-1}}\right)$
- Loss: Mean Squared Error (MSE)  
- Optimizer: AdamW  
- Early stopping enabled  

---

## Evaluation Metrics
- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  
- Mean Absolute Error (MAE)  
- R² Score  

---

## Results
The model predicts AMD closing prices based on historical patterns and entropy-driven volatility signals.

Outputs include:
- Predicted vs Actual price visualization  
- Performance metrics on test data  

---

## Tech Stack
- Python  
- NumPy, Pandas  
- Scikit-learn  
- TensorFlow / Keras  
- Matplotlib  
- yFinance  

## Limitations
- Not a production trading system  
- No macroeconomic or external features  
- No hyperparameter tuning  
- No backtesting framework  
- Predicting price does not imply profitability  

---

## Future Improvements
- Direction prediction (up/down classification)  
- Add technical indicators (RSI, MACD, Bollinger Bands)  
- Hyperparameter optimization (Optuna / Grid Search)  
- Transformer-based models  
- Backtesting and trading strategy integration  

---

## Conclusion
This project demonstrates how combining:
- sequence modeling (LSTM)  
- information theory (entropy)  

can improve financial time series representation by incorporating both structure and uncertainty.

---
