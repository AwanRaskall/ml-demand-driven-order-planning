# 📦 Forecasting product demand to optimize order planning

This Machine Learning project is dedicated to building a robust time-series forecasting model of **weekly product demand** in retail store. Based on historical sales data, the project focuses on analyzing the dependencies of several data points between themselves, taking into account trend and seasonal changes as well as studying and applying various machine learning algorithms.

The project had two **main tasks**:
1) Development a deep model and make forecast for the next 8 weeks;
2) Calculation of the optimal order volume for a given period, taking into account the probabilistic scenarios (forecast and confidence intervals) and cost of expenses (price per unit, storage cost, order cost, penalty of lost demand)

Applyed predictive modeling techniques:
- **ARIMA** - a classical statistical approach for univariate time series;
- **SARIMA** - seasonal Arima model;
- **XGBoost** - an efficient gradient boosting framework for machine learning;
- **Random Forest** - a machine learning model using lagged features and recursive prediction.

Models were trained under different seasonality assumptions (zero and 72‑week seasonal cycle) obtained after decomposition.

---

## 📁 Repository Structure
```
ml-demand-driven-order-planning/
├── product_demand_prediction.ipynb            # Python notebook of scripts
├── figures/                                   # Forecast plots and evaluation charts
├── Report/                                    # File with report in IEEE format and presentation
│ ├── Product_Demand_Forecasting_Presentation
│ └── Product_Demand_Forecasting_Report
├── .gitattributes
├── .gitignore
├── .python-version
├── requirements.txt
└── README.md
```

## 🗎 Project Structure

All code and modeling steps are contained in a single, well-documented file - `product_demand_forecasting.ipynb`. It includes data loading, feature engineering, modeling, evaluation, forecasting, and calculation of the optimal order volume.
```
product_demand_forecasting.ipynb
├── Import libraries
├── Data Import
├── First acquaintance with data
│ ├── The center description
│ └── The meal description
├── Data Preprocessing
│ ├── Data cleaning
│ ├── Detecting Outliers
│ ├── Correlational analysis
│ ├── Handling Outliers
│ ├── Seasonal–Trend Decomposition
│ └── Stationarity Check and Column Engineering
├── Modeling  
│ ├── Metrics functions
│ ├── Model creation
│   ├── ARIMA
│   ├── SARIMA
│   ├── Xgboost
│   └── Random Forest
├── Evaluation of predictions
├── Forecast
└── Calculation of the optimal order volume
```

---

## How to Run

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the desired scripts, for instance:
   ```bash
   python src/arima_forecast.py
   ```

---

## 📊 Results & Report
- Model evaluation metrics (MSE, RMSE, MAPE) are summarized in Figure & Table within the report.
- The chosen non‑seasonal XGBoost model achieved the lowest error and was used for the final 8‑week demand forecast.
- Procurement requirements per week are presented in Table 2.
- Forecast visualized with 95 % confidence intervals.

## 🧠 Design Decisions
- Seasonality analysis: autocorrelation/PACF plots (Figures 3–4), FFT spectra identifying a 72‑week cycle.
- Models built under two hypotheses: no seasonality vs. 72‑week seasonal component.
- Feature engineering: trend, lags, rolling stats, sinusoidal features for seasonality.
- Model selection: AIC/BIC for ARIMA/SARIMA, RMSE/MAPE for machine learning models.
- Hyperparameter tuning: randomized search for XGBoost and Random Forest.

## 📈 Future Work
- Explore Bayesian or grid search for hyperparameter tuning to improve model robustness (vs. current randomized search).
- Evaluate advanced temporal models such as LSTM, TCN, or Facebook Prophet.
- Incorporate exogenous features (promotions, holidays, external events) to enhance forecast accuracy.

## License
This project is licensed under the GPL-3.0 License