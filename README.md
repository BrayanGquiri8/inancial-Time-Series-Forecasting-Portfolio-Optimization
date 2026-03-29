# inancial-Time-Series-Forecasting-Portfolio-Optimization
This project demonstrates an end-to-end quantitative analysis pipeline, applying statistical hypothesis testing, machine learning forecasting, and Modern Portfolio Theory (MPT) to real-world stock market data.
### 🔍 Key Analytical Phases:

**1. Data Engineering & Stationarity Diagnostics**
* Extracted raw financial data via the `yfinance` API.
* Conducted **Augmented Dickey-Fuller (ADF) tests** to diagnose non-stationarity in raw stock prices.
* Applied mathematical transformations (differencing and percentage changes) to remove trends, achieving strict stationarity ($p-value = 0.0$) to prepare the data for predictive modeling.
* Performed **Seasonal Decomposition** to isolate underlying trends, seasonal cycles, and detect heteroscedasticity in market residuals.

**2. Predictive Modeling & Forecasting Validation**
* Engineered time series forecasting models to predict short-term stock price movements.
* Validated the models using rigorous train/test splits and alignment techniques.
* **Performance Metrics:** * Achieved an outstanding **Mean Absolute Percentage Error (MAPE)** of **< 5%** across core assets. 
    * **Walmart (WMT):** 3.54% MAPE (RMSE: $4.60)
    * **Apple (AAPL):** 3.79% MAPE (RMSE: $11.29)
    * **IBM (IBM):** 5.01% MAPE (RMSE: $15.91)

**3. Risk Management & Portfolio Optimization**
* Calculated cross-asset correlation matrices to identify diversification opportunities, revealing a highly favorable, weak positive correlation (**0.18**) between the Tech sector (IBM) and Defensive Retail (WMT).
* Built a **Minimum Variance Portfolio** using covariance algebra to mathematically minimize investment risk. 
* **Optimal Capital Allocation:** The algorithm determined an ideal risk-adjusted weighting of **60% WMT** (the defensive shield) and **40% IBM** (the growth engine).

**💡 Business Impact:** This analysis proves the ability to not only build highly accurate predictive models but also to interpret the statistical limits of algorithmic forecasting (e.g., identifying structural breaks and volatile residuals) to make sound, risk-averse financial decisions.
