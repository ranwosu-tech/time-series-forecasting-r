# Time Series Forecasting (R) – Canadian Wages

## Overview
This project applies time series forecasting techniques to monthly wage data (2001–2019). The goal is to build and evaluate forecasting models and communicate results in a clear, decision-oriented way.

## Results
- Selected **ARIMA(3,1,0)** based on **AIC/BIC** and residual diagnostics (parsimonious model with strong fit).
- Used **log transform + first differencing** to achieve stationarity (ADF improved after differencing).
- Evaluated models using **1-step-ahead rolling forecasts** (train: **2001–2010**, test: **2011–2019**) with **MSFE/MAFE**.
- Compared forecast accuracy with the **Diebold–Mariano test** (**p ≈ 0.55**), showing no significant difference vs **ARIMA(1,1,2)**, so **ARIMA(3,1,0)** was chosen for simplicity.

## Data
- **Source:** Statistics Canada (Real-Time Data Tables), **Table 14-10-0331-01**.
- **Series:** Monthly **average weekly earnings (including overtime pay)** (Canada; **all industries**; **seasonally adjusted**).
- **Time period:** **January 2001 – December 2019** (**228 monthly observations**).
- **Notes:** This series is derived from the **Labour Force Survey** and includes historical revisions in the Statistics Canada portal.

## Key Visuals
### Forecast (ARIMA)
<p align="center">
  <img src="images/forecast_arima310.png" width="700">
</p>

### Seasonality by Month
<p align="center">
  <img src="images/seasonality_by_month.png" width="700">
</p>

## Tools
- R (forecasting, diagnostics, evaluation)
- Excel (light preprocessing)

## Key Methods
- Data preparation: log transformation and differencing to support stationarity
- Model development: ARIMA (and seasonal alternatives)
- Diagnostics: residual checks and model adequacy review
- Evaluation: one-step-ahead rolling forecast and error metrics (MSFE, MAFE)
- Model comparison: statistical testing (Diebold–Mariano test)

## Deliverables
- Project report (PDF)
- Key plots (added in the `images/` folder)
- Code: Available upon request (RMarkdown)

## How to Review Quickly
1. Open the project report PDF in this repo.
2. Review the plots in `images/` (summary visuals).
3. Skim the model evaluation section for final model selection and results.
