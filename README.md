# Trader-Performance-vs-Market-Sentiment

## 📌 Overview

This project analyzes how market sentiment (Fear vs Greed) impacts trading performance.
By combining historical trading data with the Fear & Greed Index, we identify patterns in profitability, risk, and trader behavior, and build a simple machine learning model to predict trade outcomes.

---

## 📂 Project Structure

```
trading-analysis/
│
├── analysis.ipynb          # Jupyter Notebook (main analysis)
├── analysis.py                 # Script version
├── fear_greed_index.csv    # Sentiment dataset
├── historical_data.csv     # Trading dataset
├── screenshots/            # Output images
│   ├── pnl_distribution.png
│   ├── win_rate.png
│   └── confusion_matrix.png
└── README.md
```

---

## ⚙️ Setup Instructions

### 1️⃣ Create Virtual Environment (Recommended)

```
python -m venv venv
```

Activate environment:

* **Windows**

```
venv\Scripts\activate
```

* **Mac/Linux**

```
source venv/bin/activate
```

---

### 2️⃣ Install Dependencies

```
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

---

## ▶️ How to Run

### 📓 Run Notebook

```
jupyter notebook
```

Open:

```
analysis.ipynb
```

---

### 🐍 Run Python Script

```
analysis.py
```

---

## 📊 Sample Outputs

### 📈 PnL Distribution

![PnL Distribution](screenshots/pnl_distribution.png)

Shows how profit and loss varies across Fear and Greed market conditions.

---

### 📊 Win Rate by Sentiment

![Win Rate](screenshots/win_rate.png)

Indicates slightly higher win rates during Greed periods.

---

### 🔥 Confusion Matrix

![Confusion Matrix](screenshots/confusion_matrix.png)

Displays model performance in predicting profitable vs losing trades.

---

## 🧠 Methodology

* Cleaned and standardized both datasets
* Converted timestamps and aligned data by date
* Merged trading data with sentiment index
* Created features:

  * Win/Loss indicator
  * Absolute PnL (volatility proxy)
* Performed exploratory data analysis (EDA) using visualizations
* Built a **Random Forest Classifier** to predict trade profitability

---

## 📌 Key Insights

* Higher average PnL observed during **Greed** periods
* **Win rate improves slightly** in Greed markets
* **Fear periods show higher volatility and larger losses**
* Traders tend to take **larger positions during Greed**
* More cautious behavior is needed during Fear conditions

---

## 💡 Strategy Recommendations

* Reduce position size and leverage during Fear periods
* Avoid overtrading in highly volatile markets
* Increase exposure cautiously during stable Greed phases
* Use sentiment as a **supporting signal**, not a standalone strategy
* Combine with technical indicators for better decision-making

---

## 🤖 Model Details

* **Algorithm:** Random Forest Classifier
* **Objective:** Predict whether a trade will be profitable
* **Features Used:**

  * Trade size (`size_usd`)
  * Market sentiment (`classification`)

---

## 🚀 Future Improvements

* Add risk metrics (Sharpe Ratio, Drawdown)
* Try advanced models (XGBoost, LightGBM)
* Include technical indicators
* Build an interactive dashboard (Streamlit)

---

## 📬 Contact

Feel free to reach out for questions or suggestions!

---
