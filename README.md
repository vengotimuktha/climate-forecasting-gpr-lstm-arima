# Probabilistic Climate Forecasting Using GPR, LSTM & ARIMA  
**Uncertainty-Aware Time Series Modeling | Kent State University Final Project**

##  Project Overview

This project models **global land-ocean temperature trends** using advanced time series methods including:
- **Gaussian Process Regression (GPR)**  
- **ARIMA & SARIMA**  
- **LSTM (Long Short-Term Memory neural networks)**

We aimed to **forecast future temperature anomalies** and **quantify uncertainty** to support better climate risk assessment and environmental policy insights.

---

##  Objective

> How accurately can we model long-term global temperature shifts while preserving interpretability and forecasting uncertainty?

---

##  Dataset

- **Source**: Berkeley Earth Surface Temperature Dataset  
- **File**: `GlobalTemperatures.csv`  
- **Span**: Historical temperature anomalies across land and ocean  
- **Cleaning**:  
  - Removed nulls, scaled temperature fields  
  - Applied **MICE** (Multiple Imputation by Chained Equations) for missing values  
  - Normalized date/time series for ML input  

---

##  Models Implemented

| Model         | Strengths                                         | Limitations                      |
|---------------|---------------------------------------------------|----------------------------------|
| **GPR**       | Captures non-linear patterns + uncertainty bounds | Computationally intensive        |
| **ARIMA/SARIMA** | Strong for seasonal patterns                  | Limited for complex non-linear   |
| **LSTM**      | Captures deep temporal dependencies               | Less interpretable, needs tuning |

---

##  Results Summary

| Model        | RMSE   | MAE   | R² Score | Uncertainty Support |
|--------------|--------|-------|----------|----------------------|
| GPR          | **0.26** | 0.18 | 0.89     |  Yes (confidence intervals) |
| SARIMA       | 0.34   | 0.22 | 0.72     |  No                      |
| LSTM         | 0.28   | **0.17** | **0.91**     |  Partial (via dropout)   |

 **GPR provided the best balance of accuracy + interpretability**.

---

##  Visualizations

-  Forecast plots with confidence bands (GPR)
-  LSTM vs SARIMA prediction overlays
-  Residual error plots to assess model assumptions
-  Year-on-year comparison of predicted vs actuals

> _(Upload chart images to `images/` folder and embed here if needed)_

---

##  Team Contributions

| Name                   | Key Roles                                                                   |
|------------------------|------------------------------------------------------------------------------|
| **Mukthasree Vengoti** | Built & tuned GPR + LSTM models, designed uncertainty quantification strategy |
| Subhasmita Maharana    | Performed EDA, data cleaning, SARIMA tuning                                 |
| Keerthi Akhila Pasam   | Generated visualizations, aggregated evaluation metrics                     |

---

##  Notable Techniques

- `MICE`-based missing value imputation  
- Gaussian Kernel + RBF configuration in `GPR`  
- Seasonal Decomposition before ARIMA modeling  
- LSTM with early stopping and scaled training input  
- Confidence intervals via GPR posterior + dropout inference in LSTM

---

##  Real-World Relevance

This project reflects tasks found in:
-  Climate science research labs modeling global warming trends  
-  Policy-making bodies forecasting environmental impact  
-  AI teams working on **interpretable forecasting systems**

> The integration of **probabilistic methods** and **deep learning** reflects real-world hybrid forecasting pipelines used by NASA, NOAA, and IPCC-backed research.

---

##  Project Files

-  `pdm_project_code.ipynb` — Full modeling code  
-  `Final Project Report - Group 6.pdf` — Executive summary, visualizations, results  
-  `GlobalTemperatures.csv` — Cleaned historical data  
-  _Video demo removed to comply with GitHub limits — can be hosted externally_  

---

##  Keywords  
`Time Series Forecasting` `GPR` `ARIMA` `LSTM` `Climate Modeling` `Environmental Data Science` `Uncertainty Quantification` `MICE` `Python`

---

##  Academic Context

Developed for the **Predictive Data Modeling** course (Spring 2024) at **Kent State University**.
