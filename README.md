# Trader Behavior Insights - Assignment

## Objective
Explore the relationship between trader performance and market sentiment (Fear/Greed) using two datasets:
1. Bitcoin Market Sentiment Dataset
2. Historical Trader Data from Hyperliquid

## Approach
- Merged trades with Fear/Greed index on dates.
- Aggregated performance metrics (PnL, leverage, trade size).
- Compared trader outcomes in Fear vs. Greed periods using t-tests.
- Ran clustering to group traders by behavior.
- Built regression (OLS) to test sentiment's effect on PnL.

## Key Findings
- **PnL differences** exist between Fear and Greed regimes.
- **Risk-taking behavior** (higher leverage, larger sizes) clusters during Greed.
- **Statistical tests** show sentiment significantly impacts short-term performance.
- **Regression results** indicate sentiment is a weak–moderate predictor of PnL, but still useful when combined with other signals.

## Deliverables
This folder contains:
- `merged_trades_sentiment.csv` – merged dataset
- `daily_aggregates.csv`, `account_aggregates.csv` – summaries
- `sentiment_bucket_summary.csv`, `fear_vs_greed_tests.csv` – insights
- `ols_summary.txt` – regression output
- Plots (`daily_pnl_vs_sentiment.png`, `boxplot_pnl_by_sentiment.png`)

## How to Run
```powershell
python trader_sentiment_analysis.py --trades historical_data.csv --feargreed fear_greed_index.csv --outdir outputs
