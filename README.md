# Data Science Internship Assessment

## Project Overview
This project was completed as part of the Web3 Trading Team internship assessment.  
The goal was to analyze the relationship between **trader behavior** (profitability, leverage, volume, risk-taking) and **market sentiment** (Fear vs Greed).  
The analysis provides insights into how sentiment impacts trading performance and risk exposure.

---

## Project Structure
```
ds_<yourname>/
├── notebook_1.ipynb        # Main Google Colab notebook (analysis + modeling)
├── csv_files/              # Processed or intermediate CSV files
│   ├── hyperliquid_trades.csv
│   ├── fear_greed.csv
│   ├── agg_by_sentiment.csv
│   └── summary_takeaways.csv
├── outputs/                # Visual outputs (charts, plots, etc.)
│   ├── pnl_by_sentiment.png
│   ├── leverage_by_sentiment.png
│   └── rolling_pnl_sentiment.png
├── ds_report.pdf           # Summarized insights and findings
└── README.md               # Project notes and setup instructions
```

---

## Datasets
1. **Bitcoin Market Sentiment Dataset**  
   - Columns: `Date`, `Classification` (Fear / Greed)

2. **Hyperliquid Trader Data**  
   - Columns: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `closedPnL`, `leverage`, etc.

Both datasets were cleaned, standardized, and merged on date fields to align trades with daily sentiment.

---

## Methodology
- **Data Cleaning & Preprocessing**: Normalized column names, handled missing values, parsed timestamps.  
- **Feature Engineering**: Derived metrics like signed trade size, notional value, and PnL percentage.  
- **EDA & Visualization**: Compared leverage, profitability, and volume between Fear and Greed phases.  
- **Statistical Analysis**: Mann-Whitney U test and Cohen’s d effect size to measure differences.  
- **ML Model**: Logistic Regression to demonstrate how trader features can predict sentiment influence.  
- **Report**: Summarized findings into `ds_report.pdf`.

---

## Key Insights
- Traders use **higher leverage during Greed**, but this often increases volatility and potential losses.  
- **Fear phases** are characterized by smaller trade sizes and lower leverage, reflecting caution.  
- High-leverage Greed days sometimes correlate with **weaker next-day profitability**.  
- Sentiment impacts trader behavior, but does not fully determine profitability.  

---

## How to Run
1. Open `notebook_1.ipynb` in Google Colab.  
2. Upload datasets or use the provided Google Drive links.  
3. Run all cells sequentially.  
4. Processed outputs will be saved in `/csv_files/` and charts in `/outputs/`.  
5. Review summarized insights in `ds_report.pdf`.  

---

## Recommendations
- Impose leverage caps during Greed phases.  
- Monitor high-leverage Greed days as potential volatility signals.  
- Develop hedging strategies for extreme sentiment periods.  
- Combine sentiment data with technical indicators for stronger predictive power.  

---

## Author
Prepared by: **Ayush**  
Role: Computer Engineering Student, aspiring AI/ML Engineer  
