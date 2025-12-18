# 📊 Global Financial Markets Volatility Spillover Analysis System
# 全球金融市场波动溢出效应分析系统 (Python Engineering Ver.)

---
### 🧪 Academic Benchmark (R Version)
> **Looking for the statistical research prototype?**
> **想看包含 BEKK 模型和详细统计检验的学术原型？**

Please visit the R repository, which includes the advanced **BEKK-GARCH** model and granular diagnostic tests:
请访问 R 语言仓库，包含 BEKK-GARCH 模型及详细的统计诊断过程：

👉 **[Volatility-Spillover-Benchmark-R](https://github.com/shiyuanze/Volatility_Spillover_Benchmark_R)**

---

### 🚀 System Overview
This project implements a **production-ready quantitative framework** to analyze risk transmission mechanisms among global core assets (Crude Oil, Gold, Copper, and S&P 500). 

Unlike the research-focused R prototype, this Python version emphasizes **automation, scalability, and visualization**. It features an automated ETL pipeline, a dynamic network topology generator, and a robust rolling forecast engine to validate model performance in real-world scenarios.

> **Key Achievement:** Successfully identified the "Contagion Effect" during the 2020 market crash and achieved a high volatility prediction accuracy (**RMSE: 0.0011**).

---

### 🛠️ Tech Stack & Engineering
* **Core Logic:** `Python 3.10+`
* **Data Pipeline:** `yfinance`, `pandas_datareader` (Automated scraping with anti-blocking mechanisms)
* **Statistical Modeling:** `statsmodels` (VAR, Granger Causality), `arch` (GARCH Volatility)
* **Network Analysis:** `networkx` (Graph Theory for risk topology)
* **Visualization:** `matplotlib`, `seaborn` (Dual-axis & Heatmaps)
* **Validation:** `scikit-learn` (Rolling Forecast & RMSE evaluation)

---

### 🧩 System Modules (Workflow)

#### 1. Automated Data ETL (Extract, Transform, Load)
* **Smart Scraping**: Built a robust scraper for Yahoo Finance & FRED with random delays to bypass rate limits.
* **Preprocessing**: Automated stationarity checks (ADF Test) and log-return calculations.
* **Stylized Facts**: Visualized price decoupling events (e.g., 2014 Oil Crash) using dual-axis charts.

#### 2. Linear Interdependence Analysis (VAR)
* **Model Selection**: Automated lag length selection based on AIC/SIC information criteria.
* **Causality Testing**: Conducted **Granger Causality tests** to determine the directional spillover effects between commodities and equities.

#### 3. Dynamic Correlation Modeling (DCC-GARCH)
* **Volatility Modeling**: Implemented GARCH(1,1) to capture volatility clustering.
* **Dynamic Correlations**: Constructed **DCC (Dynamic Conditional Correlation)** matrices to observe how asset correlations evolve over time.
* **Crisis Detection**: Captured correlation spikes (>0.6) during the 2020 pandemic, validating the "Flight-to-Safety" and "Contagion" hypotheses.

#### 4. Risk Spillover Network (Topology)
* **Graph Construction**: Converted the correlation matrix into a weighted network graph using `NetworkX`.
* **Centrality Analysis**: Visualized the network topology to identify the **S&P 500** as the central node in the global risk transmission web.

#### 5. Robustness & Forecasting (Backtesting)
* **Rolling Forecast**: Implemented a **12-step out-of-sample rolling forecast** mechanism (simulating real-time prediction).
* **Performance Metric**: Evaluated the model using **RMSE (Root Mean Square Error)**, achieving a score of **0.0011**, proving strong predictive stability.

---

### 📈 Visualizations
* **Dual-Axis Trends**: Price movements of Oil vs. S&P 500.
* **Dynamic Correlation Plot**: Time-varying correlation coefficients (2010-2024).
* **Network Topology**: Visual structure of asset linkages.
* **Forecast vs Actual**: Red/Black line comparison showing high predictive accuracy.

---

### 🏁 How to Run
1. Clone the repository:
 git clone [https://github.com/shiyuanze/Volatility-Spillover-Analysis-System.git](https://github.com/shiyuanze/Volatility-Spillover-Analysis-System.git)

2.Install dependencies: 
pip install pandas numpy yfinance arch networkx scikit-learn seaborn statsmodels matplotlib

3.Run the main notebook:
jupyter notebook Volatility_Analysis_Python_Implementation.ipynb




