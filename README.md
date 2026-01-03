# 🌍 CO₂ Emissions Forecasting for ESG Risk Management (Time Series)

## 📌 Project Overview
This project develops a **production-ready time series forecasting system** to predict **monthly CO₂ emissions** and act as an **early warning mechanism** for ESG compliance.  
It supports proactive sustainability decision-making for manufacturing operations tied to **strict brand and regulatory commitments**.

The solution is built using **SARIMA modeling**, backed by rigorous statistical validation and business-aligned performance metrics.

---

## 🎯 Business Context & Impact
- Manufacturing partners have **binding ESG commitments** (e.g., 42% CO₂ reduction by 2030).
- Monthly emission audits directly affect **supplier ratings, penalties, and contract renewals**.
- Reactive reporting is insufficient for risk mitigation.

**Business Value Delivered**
- Enabled **1–2 month advance visibility** into CO₂ emissions.
- Supported **proactive operational adjustments** and carbon offset planning.
- Reduced ESG compliance risk by shifting from reactive to predictive monitoring.

---

## 🧠 Technical Approach
### 1. Exploratory Analysis
- Identified **upward trend**, **strong seasonality**, and **increasing variance**
- Confirmed **multiplicative time series structure**

### 2. Data Transformation
- **Box-Cox Transformation** (λ ≈ −0.66) to stabilize variance
- Regular & seasonal differencing to remove trend and seasonality

### 3. Stationarity Validation
- **Augmented Dickey-Fuller (ADF) Test**
  - p-value < 0.01 → Stationarity confirmed

### 4. Model Identification
- **ACF / PACF analysis** at lags 1 and 12
- Final model:
```text
SARIMA(1,1,1)(1,1,1)₁₂
