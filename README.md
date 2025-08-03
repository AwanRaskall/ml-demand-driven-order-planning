# 📦 Forecasting future product demand to optimize retail order planning

This Machine Learning project is dedicated to building a robust time-series forecasting model of **weekly product demand** in retail store. Based on historical sales data, the project focuses on analyzing the dependencies of several data points between themselves, taking into account trend and seasonal changes as well as studying and applying various machine learning algorithms.

The project had two **main tasks**:
1) Development a deep model and make forecast for the next 8 weeks;
2) Calculation of the optimal order volume for a given period, taking into account the probabilistic scenarios (forecast and confidence intervals) and cost of expenses (price per unit, storage cost, order cost, penalty of lost demand)

Applyed predictive modeling techniques:
- **ARIMA** - a classical statistical approach for univariate time series;
 * **SARIMA** - Seasonal Arima model;
 * **XGBoost** - an efficient gradient boosting framework for machine learning;
 * **Random Forest** - a machine learning model using lagged features and recursive prediction.

Models were trained under different seasonality assumptions (zero and 72‑week seasonal cycle) obtained after decomposition.
---

## 📁 Repository Structure
```
ml-demand-driven-order-planning/
├── product_demand_prediction.ipynb   # Python notebook of scripts
├── figures/                          # Forecast plots and evaluation charts
├── Report/                           # File with report in IEEE format and presentation
│ ├── Product_Demand_Forecasting_Presentation
│ └── Product_Demand_Forecasting_Report
├── .gitattributes
├── .gitignore
├── .python-version
├── requirements.txt
└── README.md
```
