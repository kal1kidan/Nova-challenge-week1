# Nova Financial Solutions – Week 1 Challenge

## Project Overview

This project is part of the **Nova Financial Solutions Week 1 Challenge**, focusing on financial data analysis. The challenge is divided into two main tasks:

1. **Task 1: News Sentiment Analysis (Completed)**
   - Analyzed financial news headlines to quantify sentiment.
   - Explored correlations between news sentiment and stock movements.
   - Conducted exploratory data analysis (EDA) on headline lengths, publishers, and publication times.

2. **Task 2: Quantitative Stock Analysis (Partial Progress)**
   - Prepared and loaded stock price data for multiple companies (6 CSV files).
   - Calculated technical indicators using **TA-Lib** such as SMA, RSI, and MACD.
   - Created visualizations to understand price trends and the behavior of indicators.
   - Summary statistics for key indicators have been generated.
   - Insights and deeper trend analysis are partially completed.

---

## Folder Structure

```text
├── .vscode/
│   └── settings.json
├── .gitignore
├── requirements.txt
├── README.md
├── src/
│   └── __init__.py
├── notebooks/
│   ├── task1_eda_analysis.ipynb
│   └── task2_stock_analysis.ipynb
├── data/
│   └── stock_data/  # Contains 6 CSVs for Task 2
└── scripts/
    └── __init__.py
How to Run

Clone the repository

git clone https://github.com/kal1kidan/Nova-challenge-week1.git
cd Nova-challenge-week1


Create and activate a virtual environment

python -m venv .venv
.\.venv\Scripts\activate   # Windows
source .venv/bin/activate  # Linux/Mac


Install dependencies

pip install -r requirements.txt
pip install TA-Lib


Run Notebooks

Open notebooks/task1_eda_analysis.ipynb to explore Task 1 analysis.

Open notebooks/task2_stock_analysis.ipynb to explore Task 2 partial progress.

Key Libraries Used

pandas – Data manipulation

numpy – Numerical calculations

matplotlib / seaborn – Data visualization

TA-Lib – Technical indicators for stock analysis

pynance (optional) – Financial metrics 

Notes

The raw CSV files are excluded from GitHub to avoid exceeding GitHub file size limits.

Task 2 is partially completed; technical indicators are calculated, and visualizations are prepared, but further insights and trend analysis are ongoing.

Ensure that all CSV files are present locally in data/stock_data/ to run Task 2 notebook successfully.

