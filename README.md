# 🧠 Trader Behavior & Market Sentiment Analysis

## 📊 Project Overview
This project presents a comprehensive analysis of the intricate relationship between **cryptocurrency trading behavior** and **market sentiment**.  
Using two key datasets — the **Bitcoin Fear & Greed Index** and **Hyperliquid historical trading data** — the study identifies significant contrarian patterns that can inform smarter and more profitable trading strategies.

---

## 🎯 Objective
To explore and analyze the relationship between **trader behavior** and **market sentiment** in order to uncover hidden trends, signals, and opportunities that can influence intelligent trading decisions.

---

## 📁 Project Structure


```bash
Assignment/
│
├── Data Files/                             # Given Files
│   ├── fear_greed_index.csv          
│   └── historical_dates.csv          
│
├── solution.ipynb                          # Main Code File
├── per_account_summary.csv                 # Main analysis script
├── daily_aggregates_with_sentiment.csv
│
├── requirements.tzt
│
└── README.md
```


---

## 🔬 Methodology

### **1. Data Processing Pipeline**

#### **Data Cleaning & Integration**
- Normalized timestamps with day-first format handling  
- Filtered for BTC trades and standardized symbols  
- Cleaned numeric fields (removed currency symbols, commas, etc.)  
- Mapped sentiment labels (`Fear = 0`, `Greed = 1`)  

#### **Feature Engineering**
- Daily aggregation of key trading metrics  
- Win rate and buy/sell ratio computations  
- Volatility proxies (price and PnL standard deviations)  
- Created lagged sentiment features for temporal effects  

#### **Statistical Analysis**
- Correlation analysis between sentiment and market activity  
- T-tests for group differences  
- Effect size estimation using Cohen’s *d*  
- Granger causality tests  
- Logistic regression modeling  

#### **Advanced Analytics**
- Trader segmentation using **K-means clustering**  
- Event studies around **sentiment regime shifts**  
- Predictive modeling for **PnL direction forecasting**

---

## 📊 Key Findings
- **Trading activity increases significantly during FEAR periods**, often accompanied by improved performance.  
- The data suggests **contrarian trading patterns**, where periods of fear present more favorable opportunities.

---

## 📈 Correlation Analysis

| Metric              | Correlation with Sentiment (Greed=1, Fear=0) | Interpretation |
|---------------------|----------------------------------------------|----------------|
| Unique Accounts     | **-0.433**                                   | Strong negative correlation |
| Trade Count         | -0.282                                       | Moderate negative correlation |
| Total Volume        | -0.260                                       | Moderate negative correlation |
| Net Realized PnL    | -0.216                                       | Weak to moderate correlation |

> All trading metrics show negative correlation with sentiment — trading activity and performance **increase as market sentiment becomes more fearful**.

---

## 🤖 Predictive Model Performance

- **Model Goal:** Predict next-day PnL direction  
- **Accuracy:** 79%  
- **Key Features:** Sentiment, Volume, Trade Count, Win Rate  
- **Insight:** Strong predictive power for identifying next-day market direction based on sentiment dynamics.

---

## 📞 Conclusion
This analysis reveals a **contrarian relationship** between market sentiment and trader behavior — **fear periods** often lead to higher activity, better returns, and more engaged market participants.  

The predictive model achieving **79% accuracy** reinforces the potential of **sentiment-driven trading strategies** to generate **alpha** in cryptocurrency markets.  
The statistically significant results underscore that understanding behavioral finance and sentiment cycles can be a critical edge for traders and analysts alike.

---

## ⚙️ Requirements
To reproduce the analysis, install dependencies from the `requirements.txt` file:
```bash
pip install -r requirements.txt
