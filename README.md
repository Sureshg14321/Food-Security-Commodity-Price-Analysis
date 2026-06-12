# 🌍 Global Food Security & Agricultural Commodity Analysis Dashboard

## 📌 Project Overview

The **Global Food Security & Agricultural Commodity Analysis Dashboard** is an end-to-end Business Intelligence project developed using **Python (JupyterLite)** and **Power BI**. The project analyzes agricultural commodity prices, crop production, fertilizer costs, and food security indicators to provide actionable insights into global food security trends.

The dashboard enables stakeholders, policymakers, and analysts to monitor food affordability, agricultural productivity, commodity market fluctuations, and supply chain risks through interactive visualizations and KPI metrics.

---

## 🎯 Business Problem

Food security is influenced by multiple factors such as:

- Agricultural commodity prices
- Fertilizer costs
- Crop production levels
- Food affordability
- Supply chain disruptions
- Crisis and food shock events

Organizations require a centralized analytical solution to monitor these indicators and identify emerging food security risks.

---

## 🎯 Project Objectives

- Analyze agricultural commodity price trends.
- Monitor crop production and agricultural performance.
- Evaluate fertilizer cost impacts on food systems.
- Track food security indicators.
- Identify food crisis and supply stress periods.
- Generate actionable insights through visual analytics.
- Support data-driven decision-making.

---

## 🛠️ Tools & Technologies

| Technology | Purpose |
|------------|----------|
| Python | Data Processing |
| JupyterLite | Data Cleaning & Analysis |
| NumPy | Numerical Computation |
| Pandas | Data Manipulation |
| Power BI | Dashboard Development |
| DAX | KPI Measure Creation |

---

## 📂 Datasets Used

### 1. Commodity Prices Dataset
Contains:

- Wheat Prices
- Maize Prices
- Soybean Oil Prices
- DAP Fertilizer Prices
- MOP Potash Prices
- MOM Growth %
- YOY Growth %
- Fertilizer Composite Index

**Shape:** `780 × 18`

---

### 2. Crop Yields Dataset

Contains:

- Wheat Production
- Maize Production
- Rice Production
- Agricultural Area
- Production Growth Rates
- Total Staple Production

**Shape:** `64 × 11`

---

### 3. Food Security Indicators Dataset

Contains:

- Undernourishment %
- Food Production Index
- Cereal Yield
- Arable Land %

**Shape:** `63 × 8`

---

### 4. Food Security Panel Dataset

Contains:

- Food Price Index
- Food Shock Score
- Crisis Flags
- Supply Stress Flags
- Commodity Indicators
- Affordability Metrics

**Shape:** `420 × 39`

---

## 🧹 Data Cleaning & Preprocessing

Data cleaning was performed using **JupyterLite**.

### Steps Performed

### Import Libraries

```python
import pandas as pd
import numpy as np
```

### Data Inspection

```python
df.head()
df.info()
df.describe()
df.shape
```

### Data Cleaning

- Handled missing values
- Checked duplicates
- Converted date columns
- Standardized column formats

### Feature Engineering

Created additional metrics:

- Month-over-Month Growth %
- Year-over-Year Growth %
- Fertilizer Composite Index
- Food Shock Score
- Crisis Flags
- Supply Stress Flags
- DAP-to-Wheat Ratio

### Export

Cleaned datasets were exported as CSV files and loaded into Power BI.

---

## 📊 Power BI Data Model

The Power BI model integrates four cleaned datasets using common date and year dimensions.

### Relationships

- Date-based relationships
- Year-based relationships

This enables cross-filtering and integrated analysis across all dashboard pages.

---

## 📈 DAX Measures

### Average Food Price Index

```DAX
Average Food Price Index = AVERAGE(food_security_panel_cleaned[ffpi_overall])
```

### Average Wheat Price

```DAX
Average Wheat Price = AVERAGE(commodity_prices_cleaned[wheat_usd_mt])
```

### Average Maize Price

```DAX
Average Maize Price = AVERAGE(commodity_prices_cleaned[maize_usd_mt])
```

### Average Fertilizer Index

```DAX
Average Fertilizer Index = AVERAGE(food_security_panel_cleaned[fertiliser_composite_idx])
```

### Average Crop Yield

```DAX
Average Crop Yield = AVERAGE(food_security_indicators_cleaned[cereal_yield_kg_ha])
```

### Average MOM Growth %

```DAX
Average MOM Growth % = AVERAGE(food_security_panel_cleaned[ffpi_overall_mom_pct])
```

### Average YOY Growth %

```DAX
Average YOY Growth % = AVERAGE(food_security_panel_cleaned[ffpi_cereals_yoy_pct])
```

### Crisis Count

```DAX
Crisis Count = SUM(food_security_panel_cleaned[ffpi_crisis_flag])
```

### Supply Stress Count

```DAX
Supply Stress Count = SUM(food_security_panel_cleaned[supply_stress_flag])
```

---

# 📋 Dashboard Pages

## 1️⃣ Executive Summary

### KPI Cards

- Average Food Price Index
- Average Wheat Price
- Average Maize Price
- Average Fertilizer Index
- Average Crop Yield
- Average MOM Growth %
- Average YOY Growth %
- Crisis Count

### Visuals

- Food Price Index Trend
- Food Shock Score Trend

---

## 2️⃣ Commodity Analysis

### KPI Cards

- Average Wheat Price
- Average Maize Price
- Average Fertilizer Index
- Highest Commodity

### Visuals

- Commodity Price Trend
- Fertilizer Composite Index Trend
- DAP-to-Wheat Ratio Trend
- Food Price YOY Growth Trend

---

## 3️⃣ Agriculture Analysis

### KPI Cards

- Average Crop Yield
- Highest Production
- Lowest Production
- Average Cereal Yield

### Visuals

- Crop Production Trend
- Total Staple Production
- Fertilizer Index Trend
- Crop Area Trend

---

## 4️⃣ Food Security Analysis

### KPI Cards

- Crisis Count
- Supply Stress Count
- Average Food Shock Score
- Average Undernourishment %

### Visuals

- Food Crisis Events by Year
- Supply Stress Events by Year
- Undernourishment Trend
- Food Production Index Trend

---

## 💡 Key Insights

### Commodity Analysis

- Soybean Oil recorded the highest average market price.
- Fertilizer prices experienced significant volatility after 2008.
- Commodity prices showed sharp fluctuations during global disruptions.

### Agriculture Analysis

- Wheat contributed the highest production among staple crops.
- Total staple production increased steadily over time.
- Agricultural land allocation remained relatively stable.

### Food Security Analysis

- Food crisis events increased during major price shocks.
- Supply stress events aligned with fertilizer price spikes.
- Food production index demonstrated long-term growth.

### Executive Summary

- Average Food Price Index remained relatively stable.
- Crisis and supply stress events affected food affordability.
- Agricultural productivity improved despite commodity volatility.

---

## 🚀 Conclusion

This project successfully integrated commodity prices, crop production data, fertilizer indicators, and food security metrics into a unified analytical dashboard.

The solution provides:

- Real-time analytical insights
- Food security monitoring
- Agricultural performance tracking
- Commodity trend analysis
- Data-driven decision support

---



