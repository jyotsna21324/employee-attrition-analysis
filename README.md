# Employee Attrition Analysis

Analysis of the IBM HR Analytics Employee Attrition dataset to identify the factors most associated with employee turnover, using Python for data cleaning and KPI derivation, SQL for querying, and matplotlib for visualization.

## Objective

Identify which departments, roles, and employee characteristics correlate most strongly with attrition, and translate that into a risk-flagging framework that could support HR retention decisions.

## Data Source

IBM HR Analytics Employee Attrition & Performance dataset — a publicly available dataset of 1,470 employee records with 35 attributes covering demographics, compensation, tenure, and satisfaction scores.

## Repository Structure

```
├── data/
│   ├── WA_Fn-UseC_-HR-Employee-Attrition.csv   Raw dataset
│   ├── cleaned_attrition_data.csv              Cleaned dataset with engineered features
│   ├── attrition_by_department.csv
│   ├── attrition_by_jobrole.csv
│   ├── feature_comparison.csv
│   ├── correlation_matrix.csv
│   └── powerbi_ready_data.xlsx                 Formatted for Power BI import
├── scripts/
│   ├── 01_data_cleaning.py
│   ├── 02_kpi_analysis.py
│   ├── 03_attrition_overview_chart.py
│   ├── 04_department_chart.py
│   ├── 05_jobrole_chart.py
│   ├── 06_overtime_chart.py
│   ├── 07_income_chart.py
│   ├── 08_tenure_satisfaction_chart.py
│   └── 09_correlation_heatmap_chart.py
├── sql/
│   ├── attrition_analysis.sql
│   └── attrition_database.db
└── visuals/
    ├── 01_overall_attrition.png
    ├── 02_attrition_by_department.png
    ├── 03_attrition_by_jobrole.png
    ├── 04_overtime_vs_attrition.png
    ├── 05_income_distribution.png
    ├── 06_tenure_satisfaction.png
    └── 07_correlation_heatmap.png
```

## Tools Used

Python (pandas, numpy, matplotlib), SQL (SQLite), Power BI (data import)

## Key Findings

- Overall attrition rate: **16.1%** (237 of 1,470 employees)
- Highest attrition by department: **Sales (20.6%)**, followed by HR (19.1%); R&D is lowest (13.8%)
- Highest attrition by role: **Sales Representatives (39.8%)** — by far the highest-risk role
- Employees working **overtime** attrite at **30.5%** vs **10.4%** for those who don't
- Employees earning **under 3K/month** attrite at **28.6%** vs **3.8%** for 15K+ earners
- Employees with **0-1 year tenure** attrite the most at **34.9%**, dropping steadily with tenure
- Total working years, monthly income, and age show the strongest negative correlation with attrition — more experienced, better-paid, older employees are least likely to leave

## How to Run

```
cd scripts
python3 01_data_cleaning.py
python3 02_kpi_analysis.py
python3 03_attrition_overview_chart.py
python3 04_department_chart.py
python3 05_jobrole_chart.py
python3 06_overtime_chart.py
python3 07_income_chart.py
python3 08_tenure_satisfaction_chart.py
python3 09_correlation_heatmap_chart.py
```

SQL queries can be run against `sql/attrition_database.db` using any SQLite client.
