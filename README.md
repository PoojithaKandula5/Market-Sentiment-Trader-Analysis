# Trader Performance vs Market Sentiment Analysis

## Objective

The goal of this project is to analyze how market sentiment (Fear vs Greed) influences trader behavior and performance.
By combining sentiment data with real trading activity, we aim to uncover patterns that can inform better trading decisions.

---

## Datasets Used

### 1. Bitcoin Market Sentiment Dataset

* Columns: `timestamp`, `value`, `classification`, `date`
* Represents daily market sentiment (Fear or Greed)

### 2. Hyperliquid Trader Dataset

* Columns include:

  * `Account`
  * `Size USD`
  * `Side` (BUY/SELL)
  * `Closed PnL`
  * `Timestamp IST`
  * and other trade-related attributes

---

## Methodology

### Data Preparation

* Loaded datasets using Pandas
* Cleaned column names and handled formatting issues
* Converted timestamps to datetime format
* Extracted date and merged datasets on daily level
* Checked for missing values and duplicates

---

### Feature Engineering

Created key metrics for analysis:

* Daily PnL per trader
* Number of trades per day (trade frequency)
* Average trade size
* Long/Short ratio (BUY vs SELL behavior)
* Trade size categorization (Large vs Small)

---

### Analysis Performed

#### 1. Performance vs Sentiment

* Compared PnL distribution across Fear and Greed periods
* Observed differences in profitability and volatility

#### 2. Behavior vs Sentiment

* Analyzed how traders change:

  * Trade size
  * Trade direction (long/short)
  * Trading activity

#### 3. Trader Segmentation

* High vs Low trade size traders
* Frequent vs Infrequent traders
* Winners vs Losing traders

---

## Key Insights

1. **Market sentiment strongly impacts trader performance**

   * Traders tend to experience higher volatility during Fear periods.

2. **Risk-taking behavior increases during Greed periods**

   * Traders use larger trade sizes and show a higher tendency to go long.

3. **High-frequency and large-size traders exhibit unstable performance**

   * Overtrading and excessive risk lead to inconsistent results.

4. **Consistent traders maintain moderate risk and stable returns**

   * Controlled strategies outperform aggressive approaches over time.

---


## How to Run

### 1. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 2. Add Dataset Files

Place the following files in the project folder:

* `fear_greed.csv`
* `trader_data.csv`

---

### 3. Run the Notebook

```bash
jupyter notebook market_sentiment_trader_analysis.ipynb
```

OR open in Google Colab and run all cells.

---

## Output

The notebook includes:

* Cleaned and processed datasets
* Visualizations (boxplots, bar charts, distributions)
* Behavioral analysis
* Actionable insights and strategies

---

## Conclusion

Market sentiment plays a critical role in shaping trader behavior and performance.
By understanding these patterns, traders can reduce risk, avoid emotional decisions, and improve long-term consistency.
