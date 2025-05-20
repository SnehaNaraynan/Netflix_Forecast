# Netflix UCAN Revenue & ARPU Forecasting (Q1 2025)

This project forecasts Netflix's **Average Revenue Per User (ARPU)** and **Streaming Revenue** in the **U.S. and Canada (UCAN)** region using time series models — **Prophet** and **ARIMA**. The goal is to analyze revenue dynamics, anticipate the impact of policy changes (e.g., the household plan), and assess model performance through forecast accuracy.

---

## Objective

- Forecast Q1 2025 UCAN ARPU and Streaming Revenue.
- Compare model performance using actual revenue data (ARPU still pending).
- Evaluate Prophet and ARIMA for short-term business forecasting.
- Translate predictions into actionable business insights.

---

## Models Used

| Model   | Description |
|---------|-------------|
| **Prophet** | Additive model by Meta designed for trend + seasonality |
| **ARIMA (1,1,1)** | Traditional time series model suited for stable trends and small fluctuations |

---

## Key Metrics

| Metric | Description |
|--------|-------------|
| **UCAN ARPU** | Average revenue per subscriber (in USD) |
| **UCAN Streaming Revenue** | Total regional revenue from Netflix streaming (USD) |
| **% Error** | Accuracy of model forecast compared to actual data |
| **MAE, RMSE, MAPE** | Prophet model evaluation metrics (historical fit) |

---

## Key Dimensions

- **Time**: Quarterly data (up to Q1 2025)
- **Region**: UCAN (U.S. and Canada)
- **Model Type**: Prophet, ARIMA
- **Metric Type**: Revenue vs ARPU

---

## Results Summary

### UCAN Streaming Revenue (Q1 2025)

| Model   | Forecasted Revenue | Actual Revenue | % Error |
|---------|---------------------|----------------|---------|
| Prophet | \$4,457,885,000     | \$4,625,884,000 | 3.63% |
| ARIMA   | \$4,608,102,000     | \$4,625,884,000 | **0.38%** ✅ |

 *Actual UCAN revenue value sourced from Netflix’s official earnings report:*  
[Netflix Q1 2025 Earnings](https://ir.netflix.net/financials/quarterly-earnings/default.aspx)

---

### UCAN ARPU (Q1 2025 – Forecast Only)

| Model   | Forecasted ARPU |
|---------|------------------|
| Prophet | \$17.84 |
| ARIMA   | \$17.37 |

*ARPU for Q1 2025 has not been published yet. These are provisional estimates and will be validated once official figures are released.*

---

### Prophet Model Evaluation (Historical)

- **MAE**: 0.19
- **RMSE**: 0.23
- **MAPE**: 1.37%

These scores indicate strong performance and minimal error when fitting past ARPU trends.

---

## Business Insights

- **ARIMA** closely matched actual UCAN revenue, confirming the model’s suitability for steady revenue forecasting.
- **Prophet** captured trend + seasonality well and slightly overestimated Q1 2025 revenue.
- ARPU predictions suggest Netflix may see stable or slightly rising per-user income, but this remains to be confirmed.
- If actual ARPU comes in lower than forecasted (\< \$17.84), it may reflect growing user base with lower per-user yield — possibly due to household plan adoption.

---

## Tech Stack

- Python
- pandas, numpy
- Prophet
- statsmodels (ARIMA)
- scikit-learn (metrics)
- matplotlib
