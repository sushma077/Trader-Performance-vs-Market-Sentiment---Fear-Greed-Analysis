# Trader-Performance-vs-Market-Sentiment---Fear-Greed-Analysis
## Trader Performance vs Market Sentiment


### Problem Statement

The objective of this project is to analyze how market sentiment (Fear vs Greed) influences trader behavior and performance on the Hyperliquid trading platform, and to derive actionable trading strategies based on these insights.

### Data Description

--Bitcoin Market Sentiment Dataset

  Includes daily sentiment labels (Fear, Extreme Fear, Greed) with UNIX timestamps.
  
  Link: https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing
  
  
--Hyperliquid Historical Trader Data

  Contains individual trade records including account, side, size, PnL, fees, and timestamps in  IST format.
  
  Link: https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing
  

### Methodology

1.Data Cleaning & Alignment

--Converted UNIX timestamps and IST timestamps to a common daily date format.

--Checked for missing values, duplicates, and malformed timestamps.

--Aligned trader activity with market sentiment at daily granularity.

2.Feature Engineering

--Daily PnL per trader

--Win rate

--Trade frequency

--Average trade size

--Long/Short bias

--Fee accumulation

3.Analysis

--Compared trader performance across Fear vs Greed days.

--Studied behavioral changes in trading frequency and directional bias.

--Segmented traders based on activity and consistency.

4.Advanced Analysis

--Clustered traders into behavioral archetypes using KMeans.

--Built a baseline model to predict daily profitability.

### Key Insights

--Trader PnL is more volatile during Fear days.

--Frequent traders outperform infrequent traders during Greed regimes.

--Inconsistent traders suffer larger drawdowns during Fear periods.

--Distinct trader archetypes exhibit different risk-return profiles.

## Model Used

## --Random Forest Classifier

### Why this model was selected:

--Handles non-linear relationships between features

--Robust to noise and outliers

--Requires minimal feature scaling

--Provides strong baseline performance with limited tuning

### Results Interpretation

--Accuracy achieved: 95%

--The model achieved reasonable accuracy, indicating that trader behavior features such as win rate and trade frequency contain meaningful predictive signal.

### Limitations

--The model does not account for transaction costs beyond basic fees.

--Market conditions outside sentiment (e.g., volatility, news events) were not included.

--The dataset is limited to a specific time period and platform.


### Strategy Recommendations

1.Risk Control Strategy

---Reduce trading activity and risk exposure for low win-rate traders during Fear days.

2.Opportunity Strategy

---Increase participation for consistent, high-frequency traders during Greed periods.

### Conclusion

Market sentiment has a measurable impact on trader behavior and performance. Incorporating sentiment-aware rules can improve risk-adjusted returns and trading discipline.


## GITHUB STRUCTURE
        Trader-Performance-vs-Market-Sentiment---Fear-Greed-Analysis/
        │
        ├── trader_sentiment_analysis.ipynb
        ├── README.md
        ├── requirement.txt
        └── outputs/
            ├── graphs/
            └── tables/
        

## ▶️ Steps to Run the Notebook Locally

### 1️⃣ Clone the Repository
    git clone https://github.com/your-username/Trader-Performance-vs-Market-Sentiment---Fear-Greed-Analysis.git
    cd Trader-Performance-vs-Market-Sentiment---Fear-Greed-Analysis

### 2️⃣ Create a Virtual Environment (Recommended)
    python -m venv venv

Activate the environment:

#### Windows

    venv\Scripts\activate


#### macOS / Linux

    source venv/bin/activate

### 3️⃣ Install Dependencies
    pip install -r requirement.txt

### 4️⃣ Add the Data Files

    Place the datasets in the folder whose links are given in README.md file.
    
    Ensure the file names match those used in the notebook.

### 5️⃣ Launch Jupyter Notebook
    Open:
    
    PrimeTrade_2026.ipynb

Run all cells from top to bottom.

##### This project was developed and tested in a local Python environment to ensure full reproducibility.
