# Advanced Data Analysis Techniques — Time Series Forecasting

An advanced data analysis project applying **Seasonal Decomposition**, **Augmented Dickey-Fuller (ADF) Stationarity Testing**, **Holt-Winters Exponential Smoothing**, and **SARIMA** to 36 months of electricity demand data (`2023–2025`).

## Deliverables Included
- **Project Report (PDF):** [brother_advanced_analysis_report.pdf](reports/brother_advanced_analysis_report.pdf)
- **Implementation Notebook:** [time_series_analysis.ipynb](notebooks/time_series_analysis.ipynb)
- **Dataset:** [monthly_energy_demand.csv](data/monthly_energy_demand.csv)

## Repository Structure

    advanced-time-series-analysis/
    ├── data/
    │   └── monthly_energy_demand.csv
    ├── notebooks/
    │   └── time_series_analysis.ipynb
    ├── reports/
    │   └── brother_advanced_analysis_report.pdf
    ├── requirements.txt
    └── README.md

## Methodology & Key Findings
- **Seasonal Decomposition:** Additive decomposition (12-month period) isolates a steady year-over-year upward trend and recurring July summer peaks driven by cooling demand (`r = 0.881` correlation with `Avg_Temp_C`).
- **Validation Performance (Jul–Dec 2025 Holdout):**
  - **3-Month Moving Average (Baseline):** MAE = `2,480.6 MWh`, RMSE = `2,693.7 MWh`, MAPE = `13.84%`
  - **Additive Trend + Seasonal Model:** MAE = **`141.7 MWh`**, RMSE = **`156.4 MWh`**, MAPE = **`0.77%`**
- **2026 Outlook:** Projected demand dips to `15,838 MWh` in February 2026 before climbing to `22,288 MWh` by June 2026.
