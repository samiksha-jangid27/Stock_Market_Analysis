# 📊 Indian Banking Sector Stock Market Analysis (2020–2025)

This project presents a structured risk–return analysis of five major Indian banking stocks using historical OHLCV data from January 2020 to October 2025.

The objective is to build a unified analytical framework to support informed buy/hold/sell decisions using performance, volatility, liquidity, and momentum indicators.

---

## 🎯 Project Objective

- Analyze comparative performance across major Indian banking stocks
- Develop a risk–return segmentation framework
- Identify liquidity-backed price signals
- Study volatility and seasonal patterns
- Build an executive decision-support dashboard

---

## 📂 Dataset Overview

- **Source:** Kaggle – Indian Banking Stock Dataset  
- **Time Period:** Jan 2020 – Oct 2025  
- **Stocks Covered:** SBI, ICICI Bank, HDFC Bank, Axis Bank, Kotak Mahindra Bank  
- **Original Rows:** 7,252  
- **Working Rows (after cleaning):** 7,245  
- **Columns:** 17  
- **Data Type:** OHLC + Volume  

**Goal:** Prepare dataset for professional risk–return analysis and dashboard deployment.

---

## 🧹 Data Cleaning & Preprocessing

### Data Validation
- Removed invalid and duplicate date entries
- Validated OHLC price consistency
- Cleaned corrupted volume records (~2%)
- Standardized numerical formatting

### Handling Errors
- Treated `#VALUE!` errors in computed columns
- Ensured no missing values in final analytical dataset

---

## ⚙ Feature Engineering

The following derived metrics were created for deeper analysis:

- **Daily Return %**  
  `(Close - Previous Close) / Previous Close`

- **Intraday % Change**  
  `(Close - Open) / Open`

- **High–Low Range %**  
  `(High - Low) / Low`

- **7-Day Moving Average**

- **7-Day Rolling Volatility**

- **Win Rate (%)**  
  Percentage of positive closing days

- **Risk Level Classification**  
  High / Medium / Low (based on volatility clustering)

---

## 📊 KPI & Metrics Framework

The analysis is structured around the following KPIs:

- **5-Year Price Growth %**
- **Average Daily Return**
- **Win Rate (Up Day %)**
- **Average Daily Volume (Millions)**
- **High–Low Volatility %**
- **Volume–Price Correlation**

These KPIs collectively evaluate performance, consistency, liquidity, and risk exposure.

---

## 📈 Key Insights

- **SBI delivered the highest 5-year return (+180%)**, driven by post-COVID PSU recovery.
- **ICICI Bank showed strong private-sector growth (+150%)** with balanced risk.
- **Kotak Mahindra demonstrated lowest volatility and highest consistency**, suitable for defensive portfolios.
- **High-volume spikes precede major price movements in 78% of observed cases.**
- **Q1 (Jan–Mar) shows highest volatility**, while Q3 (Jul–Sep) exhibits strongest directional momentum.
- Volume-backed breakouts are stronger and more sustainable than low-volume rallies.

---

## 📊 Advanced Analysis

### Risk vs Return Segmentation

Stocks were segmented into strategic categories:

- **Growth / Aggressive:** SBI  
- **Growth / Balanced:** ICICI  
- **Value / Moderate:** Axis  
- **Income / Defensive:** HDFC  
- **Conservative / Stable:** Kotak  

This framework supports portfolio construction based on risk appetite.

---

## 📊 Dashboard Overview

The dashboard contains two primary layers:

### Executive View
- Total records analyzed
- Best performer (5-year)
- Most liquid stock
- Most stable stock
- Optimal risk–return balance

### Operational View
- Price growth comparison
- Volatility tracking
- Monthly return drilldowns
- Volume band analysis
- Seasonal pattern visualization

---

## 💡 Recommendations

1. **Overweight SBI & ICICI for growth-focused portfolios**
2. **Use volume spikes as entry/exit signals**
3. **Allocate Kotak Mahindra as portfolio stabilizer (15–20%)**
4. **Apply seasonal rebalancing strategy**
5. **Monitor HDFC for liquidity-backed value opportunities**

---

## 📈 Impact & Value

- **Max Observed Return:** 180% (SBI, 5-year)
- **Signal Accuracy (Volume → Price Move):** 78%
- **Coverage:** 5 Major Banking Stocks
- **Records Analyzed:** 7,245+

### Business Value

- Enables faster portfolio positioning decisions
- Reduces manual stock screening effort
- Improves risk-adjusted allocation strategy
- Supports data-driven investment planning

---

## ⚠ Limitations

- Limited to 5 major banking stocks
- No macroeconomic variables included
- No intraday tick-level data
- Historical analysis only (no live feed)

---

## 🚀 Future Scope

- Implement ML-based price forecasting (LSTM / Prophet)
- Expand to full Nifty Banking index
- Integrate macroeconomic indicators (RBI rates, inflation)
- Deploy real-time dashboard
- Add institutional-grade risk metrics (Sharpe, Beta, Drawdown)

---

## 🛠 Tools Used

- Google Sheets
- Pivot Tables
- Data Cleaning & Aggregation
- Dashboard Design (Canva)
- GitHub Version Control

---

## 📌 Final Conclusion

The analysis confirms that:

- Volume-backed momentum is a strong signal for directional moves.
- Risk-adjusted performance differs significantly across banks.
- Portfolio segmentation improves strategic allocation.
- Liquidity and volatility together provide stronger insight than price alone.

This project delivers a structured, data-driven framework for comparative banking sector investment analysis.
