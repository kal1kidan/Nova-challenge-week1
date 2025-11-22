# Stock Analysis Dashboard – Task 1 to Task 3

## Project Overview
This repository contains a comprehensive analysis of stock prices and financial news for multiple companies, covering three main tasks:

1. **Task 1 – Exploratory Data Analysis (EDA)**
   - Clean, inspect, and visualize stock price data.
   - Identify trends, missing data, and basic statistics.
   - Data sources: six stock CSV files (`AAPL.csv`, `AMZN.csv`, `GOOG.csv`, `META.csv`, `MSFT.csv`, `NVDA.csv`).

2. **Task 2 – Quantitative Analysis**
   - Calculate technical indicators using **TA-Lib**: SMA, RSI, MACD.
   - Visualize stock price trends alongside indicators.
   - Insights into stock behavior based on indicators.
   - Organized code in **modular functions** inside `src/technical_analysis.py` for reusability.

3. **Task 3 – Correlation Between News and Stock Movement**
   - Perform sentiment analysis on news headlines using **TextBlob**.
   - Align news sentiment with daily stock returns.
   - Compute correlation between sentiment and stock price movement.
   - Code organized in `src/news_correlation.py` for modularity.

---

## Repository Structure
```

Nova-Financial-Solutions-week-1/
│
├── .github/                   # GitHub Actions workflows
│   └── workflows/
│       └── unittests.yml
├── .gitignore
├── README.md
├── requirements.txt           # Project dependencies
├── src/                       # Modular Python package
│   ├── **init**.py
│   ├── technical_analysis.py  # Functions/classes for Task 2
│   ├── news_correlation.py    # Functions/classes for Task 3
│   └── utils.py               # Helper functions for loading data & plotting
├── notebooks/                 # Jupyter notebooks for Tasks 1–3
│   ├── Task1_EDA.ipynb
│   ├── Task2_TechnicalAnalysis.ipynb
│   └── Task3_NewsCorrelation.ipynb
├── data/                      # CSV datasets
│   ├── stock_data/
│   │   ├── AAPL.csv
│   │   ├── AMZN.csv
│   │   ├── GOOG.csv
│   │   ├── META.csv
│   │   ├── MSFT.csv
│   │   └── NVDA.csv
│   └── raw_analyst_ratings.csv
└── scripts/                   # Optional scripts to run notebooks or analyses
├── run_task2.py
└── run_task3.py

````

---

## Installation & Setup

1. **Clone the repository**
```bash
git clone <your-repo-link>
cd Nova-Financial-Solutions-week-1
````

2. **Create a virtual environment**

```bash
python -m venv .venv
```

3. **Activate the virtual environment**

* Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

* macOS/Linux:

```bash
source .venv/bin/activate
```

4. **Install dependencies**

```bash
pip install -r requirements.txt
```

5. **Verify installation**

```bash
python -c "import talib, textblob, pandas; print('All dependencies installed')"
```

---

## Usage

### **Task 1 – EDA**

* Open `notebooks/Task1_EDA.ipynb`.
* Inspect stock data, visualize trends, and check missing values.

### **Task 2 – Technical Analysis**

* Modular code in `src/technical_analysis.py`:

```python
from src.technical_analysis import compute_indicators, plot_sma_macd

dfs_stocks = load_stock_data('../data/stock_data/')
dfs_indicators = compute_indicators(dfs_stocks)
plot_sma_macd(dfs_indicators['AAPL.csv'])
```

* Notebooks demonstrate calculations and plots for all 6 stocks.

### **Task 3 – News Correlation**

* Modular code in `src/news_correlation.py`:

```python
from src.news_correlation import compute_sentiment, merge_with_returns, compute_correlation

df_news = load_news_data('../data/raw_analyst_ratings.csv')
dfs_corr = merge_with_returns(dfs_returns, df_news)
compute_correlation(dfs_corr)
```

* Notebook provides detailed analysis and correlation results.

---

## Key Insights

1. **Task 1**

   * Basic trends observed in each stock (uptrends, volatility spikes).
2. **Task 2**

   * SMA and MACD indicate trend reversals and momentum.
   * RSI identifies potential overbought/oversold periods.
3. **Task 3**

   * News sentiment shows weak-to-moderate correlation with daily returns.
   * Some spikes in sentiment precede significant stock movement.

---

## KPIs

* **Proactivity:** Explored multiple libraries (TA-Lib, TextBlob, pandas).
* **Modularity:** Logic organized in `src/` package for reusability.
* **Reproducibility:** Notebook logic can be executed with provided scripts.
* **Analysis:** Covers EDA, technical analysis, and sentiment correlation.

---

## References

* [TA-Lib Documentation](https://mrjbq7.github.io/ta-lib/)
* [TextBlob Documentation](https://textblob.readthedocs.io/en/dev/)
* [Pandas Documentation](https://pandas.pydata.org/docs/)
* [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)

---

✅ **Notes**

* All calculations are performed in Python using a modular approach.
* Follow the notebook order: **Task1 → Task2 → Task3**.
* Daily returns and sentiment scores are aligned by date for correlation analysis.

