# Data-science-intern-project
Analyze how market sentiment relates to trader behavior and performances on hyper liquid using Python
## Overview

This project analyzes the relationship between **Bitcoin market sentiment (Fear vs Greed)** and **trader behavior/performance** using historical trading data from Hyperliquid.

The goal is to identify how sentiment impacts:

* Trader profitability
* Trading behavior
* Risk-taking patterns

Insights from this analysis can help design **better trading strategies and risk management rules**.


---

# Setup Instructions

## 1. Clone the repository

```bash
https://github.com/Adnan-16/Data-science-intern-project.git
```

---

## 2. Create a virtual environment (recommended)

```bash
python -m venv venv
```

Activate environment

**Mac/Linux**

```bash
source venv/bin/activate
```

**Windows**

```bash
venv\Scripts\activate
```

---

## 3. Install dependencies

```bash
pip install -r requirements.txt
```

Example `requirements.txt`

```
pandas
numpy
matplotlib
seaborn
jupyter
```

---

# Dataset

Two datasets are used in this project.

### 1. Bitcoin Market Sentiment (Fear/Greed)

Contains daily sentiment classification.

Columns:

* Date
* Classification (Fear / Greed)

### 2. Historical Trader Data

Contains trading activity from Hyperliquid.

Important columns:

* account
* symbol
* execution price
* size
* side
* time
* closedPnL
* leverage

---

# How to Run the Analysis

### Step 1 — Start Jupyter Notebook

```bash
jupyter notebook
```

---

### Step 2 — Open the notebook

Navigate to:

```
notebooks/Data science intern project.ipynb
```

Run all cells sequentially.

---

# Analysis Workflow

The notebook performs the following steps:

### 1. Data Preparation

* Load datasets
* Handle missing values
* Convert timestamps
* Merge datasets by date

### 2. Feature Engineering

Key metrics created:

* Daily PnL per trader
* Win rate
* Average trade size
* Trade frequency
* Leverage usage
* Long/Short ratio

---

### Insights 
  1)During Fear periods, traders show higher trade frequency but lower average PnL.
  2)During Greed periods, traders take larger position sizes, increasing volatility.
  3)High leverage traders show larger profits but higher losses.

---

### Strategy
Strategy1: Sentiment based leverage control-
            - During Fear periods reduce leverage and position size to manage downside risk.
            - During Greed periods, moderate leverage and increased long exposure may improve returns.

Strategy2: Sentiment adaptive trade direction-
            -Favor short trades during Fear markets.
            -Favor long trades during Greed markets.

  ---


  ### Conclusion
       The analysis shows that market sentiment plays a significant role in shaping trader behavior and profitablity.
