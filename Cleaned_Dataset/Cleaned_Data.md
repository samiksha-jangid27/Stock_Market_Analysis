# 🧹 Data Cleaning & Preprocessing Log  
## Banking Sector Stock Market Dataset (2020–2025)

This document records all preprocessing, cleaning, transformation, and feature engineering steps applied to the dataset before pivot table creation and dashboard visualization.

---

## 📊 Dataset Overview

- **Original Rows:** 7,252 
- **Working Rows (after filtering & standardization):** 7,245 
- **Stocks Covered:** Axis Bank, HDFC, ICICI, Kotak Mahindra, SBI  
- **Time Period:** 2020–2025  
- **Goal:** Prepare dataset for professional risk–return analysis and dashboard visualization.

---

## 🗑 Columns Removed

No columns were permanently removed from the dataset.

All original fields were either:
- Used directly for analysis
- Cleaned and standardized
- Transformed into engineered features

---

## 🧽 Data Cleaning Steps

### 1️⃣ Date Standardization
- Ensured all date values were properly formatted.
- Extracted structured time components:
  - **Month Name**
  - **Year**

**Purpose:** Enable time-based filtering, slicers, and trend analysis.

---

### 2️⃣ Numeric Formatting
The following columns were standardized to consistent decimal formatting:

- Daily Return %
- Intraday %
- High-Low % Range
- Volume % Change
- 7-Day Volatility

**Reason:** Improve calculation accuracy and dashboard readability.

---

### 3️⃣ Handling Blank / Inconsistent Values

- Checked for blank numeric fields.
- Ensured no invalid calculations (division errors).
- Verified Previous Close values for accurate return computation.

No major missing-value imputation was required as the dataset was structurally complete.

---

## ⚙ Feature Engineering

Several analytical columns were created to support pivot tables and KPI cards.

---

### 📈 1. Daily Return %

**Formula:**

```excel
=(Price - Previous Close) / Previous Close
```

**Purpose:**
- Measure daily percentage change
- Core performance metric for KPI cards

---

### ⚡ 2. Intraday %

**Formula:**

```excel
=(Close - Open) / Open
```

**Purpose:**
- Measure intraday trading movement
- Compare volatility within a single day

---

### 📊 3. High-Low Range

**Formula:**

```excel
=High - Low
```

**Purpose:**
- Capture daily trading spread

---

### 📊 4. High-Low % Range

**Formula:**

```excel
=(High - Low) / Previous Close
```

**Purpose:**
- Normalize daily range
- Enable cross-stock comparison

---

### 📦 5. Volume % Change

**Formula:**

```excel
=(Today Volume - Previous Volume) / Previous Volume
```

**Purpose:**
- Measure liquidity shift
- Identify abnormal trading activity

---

### 📉 6. 7-Day Moving Average

Calculated using rolling average of closing prices.

**Purpose:**
- Smooth price fluctuations
- Identify short-term trends

---

### 📊 7. 7-Day Volatility

Calculated as rolling standard deviation over 7 days.

**Purpose:**
- Measure short-term risk
- Support volatility trend analysis

---

### 🚦 8. Day Type Classification

Created a categorical column:

- **Up Day** → Daily Return > 0  
- **Down Day** → Daily Return < 0  
- **No Change** → Daily Return = 0  

**Purpose:**
- Used in donut chart
- Supports performance distribution analysis

---

### ⚠ 9. Risk Level Classification

Stocks were categorized into:

- **Low**
- **Medium**
- **High**

Based on volatility thresholds.

**Purpose:**
- Enable risk distribution charts
- Simplify executive-level interpretation

---

### 📅 10. Month & Year Columns

Extracted from Date column:

- Month (Full Name)
- Year (YYYY format)

**Purpose:**
- Slicers
- Time-based pivot tables
- Yearly trend chart

---

## 📊 KPI Calculations Used in Dashboard

The following KPIs were calculated using aggregated pivot logic:

- **Average Daily Return**
- **Average Intraday Return**
- **Average Volatility**
- **Total Trading Days**
- **% High Risk Days**
- **% Up Days**

These KPIs support executive-level dashboard insights.

---

## 📈 Final Dataset State

After preprocessing:

✔ Dates standardized  
✔ Time features extracted  
✔ Percentage metrics calculated  
✔ Rolling averages computed  
✔ Risk levels classified  
✔ Dataset structured for pivot tables  
✔ Fully ready for professional dashboard visualization  

---

## 📌 Conclusion

All preprocessing steps were designed to:

- Preserve analytical accuracy  
- Improve statistical consistency  
- Support dynamic pivot tables  
- Enable slicer-based filtering  
- Deliver a professional stock performance dashboard  

The dataset is now clean, structured, and optimized for risk–return analysis.
