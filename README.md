# Stock-Market-Volatility-Analysis
A quantitative study on volatility spillovers between oil, metals, and US stock indices using VAR-DCC-GARCH models (Python implementation).

# 📊 Global Financial Markets Volatility Spillover Analysis System

### 🚀 Project Overview
This project implements a comprehensive quantitative framework to analyze risk transmission mechanisms among global core assets (Crude Oil, Gold, Copper, and S&P 500). It features an automated ETL pipeline, statistical modeling (VAR, DCC-GARCH), and network topology visualization to identify systemic risk centers.

> **Key Achievement:** Successfully identified dynamic correlation shifts during the 2020 crisis and achieved a high volatility prediction accuracy (RMSE: 0.0011).

---

### 🛠️ Tech Stack & Tools
* **Data Acquisition:** `yfinance`, `pandas_datareader` (Automated scraping from Yahoo Finance & FRED)
* **Data Processing:** `pandas`, `numpy` (Time-series cleaning, Log-returns calculation)
* **Statistical Modeling:** `statsmodels` (VAR, ADF Test, Granger Causality)
* **Financial Modeling:** `arch` (DCC-GARCH for dynamic correlation)
* **Visualization:** `matplotlib`, `seaborn`, `networkx` (Dual-axis plots, Network Topology)
* **Validation:** `scikit-learn` (Rolling Forecast, RMSE evaluation)

---

### 🧩 Key Features (Modules)

#### 1. Automated Data Pipeline
* Constructed a robust scraper with anti-blocking mechanisms (random delays) to fetch 15 years of daily data.
* Implemented automated cleaning logic: Stationarity checks (ADF) and differencing for macro indicators.

#### 2. Linear Interdependence Analysis
* Built a **Vector Autoregression (VAR)** model with AIC-based optimal lag selection.
* Conducted **Granger Causality tests** to determine directional spillover effects between commodities and equities.

#### 3. Dynamic Risk Modeling (DCC-GARCH)
* Modeled time-varying correlations using **DCC-GARCH**.
* **Insight:** Captured the "Contagion Effect" during the 2020 pandemic where correlations spiked > 0.6.

#### 4. Risk Network Visualization
* Visualized the volatility spillover network using graph theory (`networkx`).
* Identified the S&P 500 as the central node in risk transmission.

#### 5. Robustness Check (Rolling Forecast)
* Implemented a **12-step Rolling Forecast** mechanism.
* Benchmarked model performance with an average **RMSE of 0.0011**, proving strong predictive validity.

---

### 📈 Sample Visualizations
<img width="737" height="644" alt="image" src="https://github.com/user-attachments/assets/d13edeb3-93e4-42d4-9c2c-6ddbe412c5ae" />
<img width="867" height="443" alt="image" src="https://github.com/user-attachments/assets/a573290f-1a8d-4cab-b544-07ba35fd2ea1" />

---

### 🏁 How to Run
1. Clone the repository.
2. Install dependencies: `pip install pandas yfinance arch networkx scikit-learn seaborn statsmodels`
3. Run `Stock-Market-Volatility-Analysis`.
