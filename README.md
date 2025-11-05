# 💼 Walmart Sales Prediction and Demand Analysis

**Technologies:** Python | Greykite | Neural Prophet | Machine Learning | Pandas | Matplotlib | Seaborn
![Python](https://img.shields.io/badge/python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/pandas-%3E%3D1.0-blue)
![Greykite](https://img.shields.io/badge/greykite-latest-green)
![NeuralProphet](https://img.shields.io/badge/neuralprophet-latest-orange)

---

## 📌 Introduction

This initiative leverages advanced Time Series Forecasting techniques through Greykite (developed by LinkedIn) and Neural Prophet (developed by Meta/Facebook) to anticipate upcoming sales trends from past performance data.

The analysis utilizes Walmart's historical sales information spanning 45 retail locations across various geographical regions, forming the basis for examining patterns, cyclical behaviors, and influencing factors such as promotional events, economic indicators, and energy costs.

---

## 🧭 Goals

The primary aim is to forecast weekly revenue figures utilizing historical records and pertinent external variables, facilitating improved stock management and strategic business planning.

---

## 🧩 Business Value

Forecasting temporal data addresses a fundamental business inquiry:

**"What can historical patterns tell us about what's ahead?"**

This methodology bridges historical data, current conditions, and future projections to reveal demand characteristics essential for:

- 📦 Streamlining supply chain operations
- 🚗 Predicting transportation service demand and fare adjustments
- 🏬 Planning retail sales strategies

For Walmart specifically, precise predictions enable enhanced stock control, strategic promotional activities, and revenue maximization during peak shopping periods and holidays.

---

## 🗂️ Data Information

**Origin:** Walmart Recruiting – Store Sales Forecasting (Kaggle Competition)

| Dataset | Contents |
|---------|----------|
| **Stores.csv** | Store characteristics including category and dimensions |
| **Train.csv** | Historical weekly revenue (Feb 5, 2010 → Nov 1, 2012) |
| **Test.csv** | Identical format to training data, excluding sales figures |
| **Features.csv** | Additional variables – Energy costs, economic indices, employment statistics, promotional discount information, holiday markers |

### Primary Variables

- **Store** – Unique store identifier
- **Dept** – Department classification
- **Date** – Week conclusion date
- **Weekly_Sales** – Revenue per week (USD)
- **IsHoliday** – Holiday occurrence indicator
- **Fuel_Price** – Local energy pricing
- **CPI** – Consumer Price Index measurements
- **Unemployment** – Local jobless rate

---

## ⚙️ Technology Stack

- **Programming Language:** Python 3.10
- **Core Libraries:** greykite, neuralprophet, scikit-learn, pandas, pandas_profiling, matplotlib, plotly, seaborn, numpy

---

## 🏗️ System Architecture
```
Raw Data (CSV Files)
    │
    ├── Data Preparation & Engineering (Analysis, missing value handling, anomaly detection)
    │
    ├── Feature Development (Temporal breakdown → Day, Month, Year + Holiday indicators)
    │
    ├── Model Construction
    │   ├── Greykite Silverkite Implementation
    │   └── Neural Prophet Implementation
    │
    ├── Performance Assessment (MAPE · RMSE)
    │
    └── Prediction Generation & Visualization (Plotly · Matplotlib · Seaborn)
```

### Key Features

- Merges statistical and deep learning approaches for reliable forecasts
- Breaks down temporal patterns into trend and seasonal elements
- Preserves trained models in output directory for future deployment
- Flexible design enables quick testing and iteration

---

## 🚀 Process & Implementation

### 1️⃣ Data Exploration

- Comprehensive feature analysis and relationship mapping using Pandas Profiling
- Identification of incomplete records and statistical outliers through Z-Score and Interquartile Range methods

### 2️⃣ Data Refinement

- Addressed gaps in promotional markdown and economic index data
- Substituted missing and invalid entries with regional average calculations

### 3️⃣ Feature Development

- Derived temporal attributes (Year, Month, Week, Day) from date stamps
- Incorporated holiday markers for seasonal pattern recognition
- Created store and regional classification mappings

### 4️⃣ Temporal Pattern Analysis

- Separated sales data into fundamental Trend and Seasonal components
- Examined impact of holidays and promotional activities

### 5️⃣ Predictive Model Construction

**🧠 Greykite Silverkite Framework**
- Automated prediction pipeline with dynamic shift detection
- Effectively captures evolving trends and recurring patterns

**🤖 Neural Prophet Framework**
- Hybrid approach combining deep learning principles with forecasting methodology
- Manages complex seasonal variations and incorporates future variables

### 6️⃣ Performance Evaluation

- **Assessment Metrics:** MAPE (Mean Absolute Percentage Error) · RMSE (Root Mean Square Error)
- Conducted comparative analysis between Greykite and Neural Prophet implementations

### 7️⃣ Prediction Output & Visualization

- Produced forecast visualizations for individual stores and departments
- Displayed prediction uncertainty ranges and projected trends

---

## 🧰 Project Organization
```
TimeSeries-Forecasting/
│
├── input/
│   ├── features.csv
│   ├── stores.csv
│   ├── test.csv
│   └── train.csv
│
├── src/
│   ├── ML_pipeline/
│   │   ├── data_preprocessing.py
│   │   ├── feature_engineering.py
│   │   ├── model_greykite.py
│   │   ├── model_neuralprophet.py
│   │   └── evaluation.py
│   ├── engine.py
│   └── server.py
│
├── output/
│   ├── greykite_model.pkl
│   ├── neuralprophet_model.pkl
│   └── forecast_results.csv
│
├── lib/
│   └── reference_notebooks.ipynb
│
├── requirements.txt
└── README.md
```

---

## 📦 Setup Instructions

Install required packages:
```bash
pip install -r requirements.txt
```

**Note:** For installing greykite and neuralprophet, please consult the "Installation Guide for Greykite and Neural Prophet" section in the project documentation.

---

## 🧪 Project Outcomes

✅ Thorough analysis of temporal sales patterns and behaviors  
✅ Successfully built dual-model forecasting system combining Greykite and Neural Prophet  
✅ Advanced feature creation incorporating holidays and trend decomposition  
✅ Applied rigorous validation using MAPE and RMSE metrics  
✅ Integrated Flask API for forecast deployment (server.py)

---

## 🧠 Planned Improvements

- Integrate gradient boosting methods (XGBoost, LightGBM) for ensemble predictions
- Implement automated hyperparameter optimization using Optuna framework
- Expand feature set with additional economic variables (fuel pricing, macroeconomic metrics)
- Build interactive visualization dashboard with Streamlit or Plotly Dash

---
