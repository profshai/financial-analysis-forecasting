# End-to-End Financial Analysis and Forecasting Portfolio Project

## Project Overview

This project is a full end-to-end financial analysis and forecasting case study built with Python. It is designed for financial analyst, FP&A analyst, revenue analyst, business analyst, forecasting analyst, and data analyst roles.

The project uses simulated company-level financial data to analyze revenue performance, profitability, margins, budget variance, customer concentration, working capital, cash flow, and revenue forecasting.

The goal is to show that I can move beyond basic charts and answer business questions that matter to finance teams.

---

## Business Problem

A growing technology and services company wants to understand:

1. What is driving revenue growth?
2. Which products, regions, and sales channels are most profitable?
3. Where is the company missing or beating budget?
4. Are discounts helping revenue or hurting margins?
5. Which customers contribute the most revenue?
6. How efficiently is the company converting sales into cash?
7. Can monthly revenue be forecasted accurately?
8. What actions should leadership take?

---

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly
- Scikit-learn
- Statsmodels
- Jupyter Notebook

---

## Repository Structure

```text
financial-analysis-forecasting-portfolio/
│
├── README.md
├── requirements.txt
│
├── data/
│   ├── README.md
│   ├── simulated_financial_transactions.csv
│   ├── monthly_budget_targets.csv
│   ├── monthly_financial_statements.csv
│   ├── macro_indicators_monthly.csv
│   └── data_dictionary.csv
│
├── notebooks/
│   └── 01_end_to_end_financial_analysis_forecasting.ipynb
│
├── figures/
│   └── Generated charts saved here
│
├── outputs/
│   └── Cleaned data, summary tables, forecasts, and model results saved here
│
└── scripts/
    └── generate_financial_data.py
```

---

## Dataset Description

The project includes four main simulated datasets.

### 1. Invoice-Level Transactions

`simulated_financial_transactions.csv`

This file contains transaction-level financial data, including:

- Invoice date
- Region
- Product line
- Sales channel
- Customer segment
- Industry
- Units sold
- Unit price
- Discount rate
- Net revenue
- Cost of goods sold
- Gross profit
- Gross margin
- Payment terms
- Days to collect
- Return flag

### 2. Monthly Budget Targets

`monthly_budget_targets.csv`

This file contains budgeted revenue, cost, gross profit, units, and discount assumptions by month, region, and product line.

### 3. Monthly Financial Statements

`monthly_financial_statements.csv`

This file contains company-level monthly financial metrics:

- Revenue
- COGS
- Gross profit
- Operating expenses
- EBITDA
- Operating income
- Net income
- Accounts receivable
- Inventory
- Accounts payable
- Capital expenditures
- Free cash flow

### 4. Macroeconomic Indicators

`macro_indicators_monthly.csv`

This file contains simulated external variables used for forecasting:

- Interest rate
- Inflation rate
- Unemployment rate
- Business confidence index
- Market index
- Exchange rate index

---

## Core Financial Metrics

The project calculates and interprets:

| Metric | Formula |
|---|---|
| Gross Profit | Revenue minus COGS |
| Gross Margin | Gross Profit divided by Revenue |
| EBITDA Margin | EBITDA divided by Revenue |
| Net Margin | Net Income divided by Revenue |
| Revenue Growth | Current Revenue divided by Prior Revenue minus 1 |
| Budget Variance | Actual minus Budget |
| Budget Variance Percent | Actual divided by Budget minus 1 |
| Average Selling Price | Revenue divided by Units |
| Discount Rate | Discount divided by Gross Price |
| Days Sales Outstanding | Accounts Receivable divided by Revenue times Days in Month |
| Inventory Days | Inventory divided by COGS times Days in Month |
| Payables Days | Accounts Payable divided by COGS times Days in Month |
| Cash Conversion Cycle | DSO plus Inventory Days minus Payables Days |
| Free Cash Flow Margin | Free Cash Flow divided by Revenue |

---

## Analysis Sections

The notebook is organized as a professional financial analytics workflow.

### 1. Data Loading and Initial Inspection

The analysis begins by loading all CSV files and checking:

- Dataset shape
- Column names
- Missing values
- Duplicate records
- Data types
- Date fields

### 2. Data Cleaning

The raw transaction data intentionally includes common real-world problems:

- Duplicate rows
- Missing values
- Inconsistent text spacing
- Missing discount rates
- Missing gross margin values
- Outlier invoices

The notebook cleans these issues and creates analysis-ready data.

### 3. Executive KPI Dashboard

The project calculates headline finance KPIs:

- Total revenue
- Gross profit
- Gross margin
- EBITDA
- EBITDA margin
- Net income
- Net margin
- Free cash flow
- Return rate
- Average days to collect

### 4. Revenue Analysis

The notebook analyzes revenue by:

- Product line
- Region
- Sales channel
- Customer segment
- Industry
- Month and year

This helps identify the strongest sources of revenue growth.

### 5. Profitability Analysis

The project studies:

- Gross profit by product line
- Gross margin by product line
- EBITDA margin over time
- Product lines with high revenue but weak margins
- Discount impact on gross margin

### 6. Budget vs Actual Variance Analysis

The notebook joins actuals with budgets and calculates:

- Revenue variance
- COGS variance
- Gross profit variance
- Unit variance
- Variance percentage
- Favorable and unfavorable budget performance

This is especially relevant for FP&A roles.

### 7. Customer Concentration Analysis

The project identifies:

- Top customers by revenue
- Customer revenue concentration
- Share of revenue from top 10 customers
- Customer segment profitability

This helps assess business dependency risk.

### 8. Working Capital and Cash Flow Analysis

The notebook analyzes:

- Days Sales Outstanding
- Inventory days
- Payables days
- Cash conversion cycle
- Free cash flow margin

This section connects income statement performance to cash flow.

### 9. Forecasting

The notebook forecasts monthly revenue using:

- Seasonal naive baseline
- Exponential smoothing
- Machine learning regression with lagged revenue and macro indicators

Forecast performance is evaluated using:

- MAE
- RMSE
- MAPE

The model then produces a forward-looking revenue forecast.

### 10. Scenario Analysis

The project includes simple base, upside, and downside scenarios based on assumptions about:

- Revenue growth
- Margin improvement
- Cost pressure
- Cash flow conversion

---

## Example Business Questions Answered

### What drives revenue?

Revenue is driven by product mix, customer segment, pricing, sales channel, seasonality, and enterprise account activity.

### What drives profit?

Profit is driven by revenue scale, product gross margin, discount discipline, operating expense control, and product mix.

### Which products have high sales but weak margins?

The analysis compares revenue contribution against gross margin to identify products that sell well but generate weaker profitability.

### Are discounts helping or hurting?

The notebook groups transactions into discount bands and compares revenue, gross margin, return rates, and customer behavior.

### Is the company beating budget?

Budget variance analysis identifies where actual revenue and gross profit are above or below plan by month, region, and product line.

### Can revenue be forecasted?

The forecasting section compares models and produces a forward monthly revenue forecast.

---

## How to Run This Project

### 1. Clone the Repository

```bash
git clone git@github.com:profshai/financial-analysis-forecasting.git
cd financial-analysis-forecasting
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Environment

Mac or Linux:

```bash
source venv/bin/activate
```

Windows:

```bash
venv\Scripts\activate
```

### 4. Install Requirements

```bash
pip install -r requirements.txt
```

### 5. Launch Jupyter

```bash
jupyter notebook
```

Then open:

```text
notebooks/01_end_to_end_financial_analysis_forecasting.ipynb
```

---

## Outputs

The notebook saves outputs to the `outputs/` folder, including:

- Cleaned transaction data
- Executive KPI summary
- Revenue by product line
- Profitability summary
- Budget variance table
- Customer concentration table
- Forecast results
- Scenario analysis table

The notebook saves charts to the `figures/` folder.

---

## Why This Project Matters for Finance Jobs

This project demonstrates job-relevant skills for financial analysis and forecasting roles:

- Data cleaning and preparation
- Financial KPI development
- Revenue analysis
- Margin analysis
- Budget variance analysis
- Customer concentration analysis
- Working capital analysis
- Time series forecasting
- Scenario analysis
- Business communication
- Executive-level recommendations

---

## Suggested Resume Bullet

Built an end-to-end financial analysis and forecasting project in Python using simulated invoice-level and monthly financial statement data; analyzed revenue drivers, gross margins, budget variance, customer concentration, working capital efficiency, and forecasted monthly revenue using statistical and machine learning methods.

---

## Limitations

The data is simulated and does not represent any real company. However, the structure is designed to reflect realistic finance analytics tasks, including messy data, seasonality, outliers, discount behavior, budget variance, and working capital dynamics.

---

## Future Improvements

Planned extensions include:

- Power BI or Tableau dashboard
- SQL version of the analysis
- Streamlit financial dashboard
- More advanced forecasting models
- Cohort retention analysis
- Revenue bridge analysis
- Automated monthly finance reporting
- Sensitivity analysis and Monte Carlo simulation

---

## Final Takeaway

This project shows how Python can be used to perform professional financial analysis from raw data to executive insights. It combines accounting logic, financial metrics, business interpretation, and forecasting in a way that is directly relevant to finance and analytics roles.
