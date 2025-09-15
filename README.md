# Mall Analysis — Customer Segmentation & Sales Insights

A business analytics project that profiles mall customers, quantifies spend behaviors, and surfaces actionable segments for targeted marketing and store planning.

---

## Business context — why this matters
Understanding **who shops and how they spend** helps Marketing and Merchandising prioritize campaigns, tailor assortments, and improve retention. This repo shows how to transform raw spreadsheets into **segment profiles** and **decision‑ready visuals**.

---

## Problem statement
Use customer and sales data to:
- **Identify segments** with distinct spend/demographic patterns
- **Quantify segment sizes and KPIs** (e.g., avg spend, income distribution)
- **Inform actions** (personalized offers, channel mix, staffing)

---

## Repository structure
```
./mall_repo/
└─ mall-analysis/
   ├─ .git/
   │  ├─ hooks/
   │  │  ├─ applypatch-msg.sample
   │  │  ├─ commit-msg.sample
   │  │  ├─ fsmonitor-watchman.sample
   │  │  ├─ post-update.sample
   │  │  ├─ pre-applypatch.sample
   │  │  ├─ pre-commit.sample
   │  │  ├─ pre-merge-commit.sample
   │  │  ├─ pre-push.sample
   │  │  ├─ pre-rebase.sample
   │  │  ├─ pre-receive.sample
   │  │  ├─ prepare-commit-msg.sample
   │  │  ├─ push-to-checkout.sample
   │  │  ├─ sendemail-validate.sample
   │  │  └─ update.sample
   │  ├─ info/
   │  │  └─ exclude
   │  ├─ logs/
   │  │  ├─ refs/
   │  │  │  ├─ heads/
   │  │  │  │  └─ main
   │  │  │  └─ remotes/
   │  │  │     └─ origin/
   │  │  │        └─ HEAD
   │  │  └─ HEAD
   │  ├─ objects/
   │  │  ├─ info/
   │  │  └─ pack/
   │  │     ├─ pack-6f4ea53a644bc39340e276b10526f45dae2b4946.idx
   │  │     ├─ pack-6f4ea53a644bc39340e276b10526f45dae2b4946.pack
   │  │     └─ pack-6f4ea53a644bc39340e276b10526f45dae2b4946.rev
   │  ├─ refs/
   │  │  ├─ heads/
   │  │  │  └─ main
   │  │  ├─ remotes/
   │  │  │  └─ origin/
   │  │  │     └─ HEAD
   │  │  └─ tags/
   │  ├─ config
   │  ├─ description
   │  ├─ HEAD
   │  ├─ index
   │  └─ packed-refs
   ├─ data/
   │  ├─ customer_data.xlsx
   │  ├─ README.md
   │  ├─ sales_data.xlsx
   │  └─ shopping_mall_data.xlsx
   ├─ notebooks/
   │  └─ Mall_Analysis.ipynb
   ├─ reports/
   │  └─ README.md
   ├─ src/
   │  └─ __init__.py
   ├─ LICENSE
   ├─ README.md
   └─ requirements.txt
```

---

## Methods & tools (applied analytics)
- **Data cleaning & preparation:** type casting, handling missing values, standardizing categories
- **Exploratory analysis & visualization:** distributions, correlations, segment profiling
- **Segmentation & KPIs:** KMeans clustering if present in notebooks; otherwise descriptive KPIs
- **Communication:** stakeholder‑ready charts and tables

**Stack detected:** matplotlib, numpy, pandas, seaborn  
**Methods detected:** EDA & visualization

---

## Results & findings (computed directly from the files)
**Shopping Mall dataset:** `shopping_mall_data.xlsx` (sheet: `shopping_mall`) — 10 rows × 5 cols

**Correlation (numeric columns, sample):**

| feature | construction_year | area (sqm) | store_count |
| --- | --- | --- | --- |
| construction_year | 1.00 | -0.47 | -0.41 |
| area (sqm) | -0.47 | 1.00 | 0.89 |
| store_count | -0.41 | 0.89 | 1.00 |


**Sales dataset:** `sales_data.xlsx` (sheet: `sales_data`) — 99,457 rows × 7 cols
- Date range: **2021-01-01 → 2023-12-02** (column: `invoice date`)

**Customer attributes dataset:** `customer_data.xlsx` (sheet: `customer_data`) — 99,457 rows × 4 cols

---

## How to run

### 1) Environment
Create Python 3.10+ environment:
```bash
# conda
conda create -n mall_env python=3.11 -y
conda activate mall_env

# or venv
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
```

Install requirements:
```
pandas
numpy
matplotlib
seaborn
openpyxl
jupyterlab
```

### 2) Open the notebook
```bash
jupyter lab
# open the notebook(s) under /notebooks
```

### 3) Outputs
- **Figures** (EDA & segment profiles) → consider saving to `reports/figures/`
- **Tables/exports** (e.g., segment assignments) → `data/processed/` or `reports/tables/`

---

## Interpreting & reusing outputs
- Use segment/demographic summaries to **target campaigns** and **tailor assortments**
- Join segment labels with sales to compute **revenue by segment**
- Export summary tables to **Tableau/Power BI** for ongoing KPI tracking
