# Trader-Performance-vs-Market-Sentiment---Fear-Greed-Analysis
## Trader Performance vs Market Sentiment


### Problem Statement

The objective of this project is to analyze how market sentiment (Fear vs Greed) influences trader behavior and performance on the Hyperliquid trading platform, and to derive actionable trading strategies based on these insights.

### Data Description

--Bitcoin Market Sentiment Dataset
  Includes daily sentiment labels (Fear, Extreme Fear, Greed) with UNIX timestamps.
  
--Hyperliquid Historical Trader Data
  Contains individual trade records including account, side, size, PnL, fees, and timestamps in  IST format.

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

### Strategy Recommendations

1.Risk Control Strategy
---Reduce trading activity and risk exposure for low win-rate traders during Fear days.

2.Opportunity Strategy
---Increase participation for consistent, high-frequency traders during Greed periods.

### Conclusion

Market sentiment has a measurable impact on trader behavior and performance. Incorporating sentiment-aware rules can improve risk-adjusted returns and trading discipline.


## GITHUB STRUCTURE
        Trader-Sentiment-Analysis/
        │
        ├── trader_sentiment_analysis.ipynb
        ├── README.md
        ├── requirements.txt
        ├── outputs/
        │   ├── charts/
        │   └── tables/
        └── data/
            ├── sentiment.csv
            └── trades.csv
