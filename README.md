# Shopping Mall Customer Analytics — Segmentation & Sales Insights

Customer segmentation and sales analysis to inform targeted marketing, store planning, and retention strategies. End‑to‑end workflow from data cleaning to actionable insights.

---

## Business context — why this matters
Retail and mall operators need to understand **who their customers are** and **how they spend** to improve targeting, personalize offers, and optimize store mix. This project turns raw spreadsheets and an analysis notebook into insights that guide **segment‑specific marketing**, **product assortment**, and **revenue forecasting**.

---

## Problem statement
Given customer demographics, spending behavior, and sales records, **identify meaningful customer segments** and **surface drivers of spend** so decision‑makers can:
- Focus promotions on high‑response segments
- Adjust assortment and staffing to match traffic patterns
- Quantify the revenue contribution by segment and track it over time

---

## What’s in this repository
- `Mall_Analysis.ipynb` — Jupyter notebook with EDA, feature engineering, and (if present) segmentation/modeling steps.
- `shopping_mall_data.xlsx` — Customer‑level attributes (e.g., Gender/Age/Income/Spending Score).
- `sales_data.xlsx` — Transaction/sales records (columns vary; totals and date range summarized below).
- `customer_data.xlsx` — Additional customer attributes (joins/enrichment).
- Any generated figures/reports are saved to `reports/` (create as needed).

> Tip: keep raw files under `data/raw/` and save cleaned outputs to `data/processed/` for reproducibility.

---

## Methods & tools (applied analytics)
- **Data cleaning & preparation:** type casting, handling missing values, standardizing categories.
- **Exploratory analysis & visualization:** distributions, bivariate relationships, and segment profiles.
- **Segmentation (K‑Means)** on behavior/demographics to create actionable customer groups.
- **KPI definition:** average spend by segment, segment sizes, and potential uplift levers.
- **Communication:** stakeholder‑ready visuals and executive‑level takeaways in the notebook.

**Stack:** jupyter, matplotlib, numpy, pandas, scikit-learn, seaborn

---

## Results & findings (computed from the included files)
**Shopping Mall Customers** (`shopping_mall_data.xlsx`): 10 rows × 5 columns

_Key numeric summary (mean/median/min/max):_

| feature | mean | median | min | max |
| --- | --- | --- | --- | --- |
| construction_year | 1976.60 | 1976.50 | 1956.00 | 2002.00 |
| area (sqm) | 154800.00 | 139000.00 | 56000.00 | 250000.00 |
| store_count | 186.00 | 185.00 | 130.00 | 270.00 |


**Sales Data** (`sales_data.xlsx`): 99,457 rows × 7 columns
- Date range: **2021-01-01 → 2023-12-02**

**Additional Customer Data** (`customer_data.xlsx`): 99,457 rows × 4 columns

---

## How to run

### 1) Environment
Create a Python environment (3.10+ recommended) and install dependencies:
```bash
# conda
conda create -n mall_env python=3.11 -y
conda activate mall_env

# OR venv
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
```

Install packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 2) Open the analysis
```bash
jupyter lab
# open Mall_Analysis.ipynb and run all cells
```

> If your notebook saves figures/tables, set output paths like `reports/figures/` and `reports/tables/`.

### 3) Reproduce key tables locally (optional)
- Customer summary and gender distribution come directly from `shopping_mall_data.xlsx`.
- Sales totals/date range are computed from `sales_data.xlsx` if columns are present (`Sales`/`Amount` and `Date`).

---

## How to interpret & reuse outputs
- **Segment table** (if created): use means/medians per segment to design **personalized offers** and **channel mix**.
- **EDA visuals**: include 2–3 with business‑first captions in presentations (e.g., “High‑income, high‑spend cohort = VIP campaign target”).
- **CSV/Excel exports**: hand to CRM for targeted campaigns or to BI tools (Tableau/Power BI) for ongoing monitoring.

---

## Evidence of Business Analytics skills
- **Data storytelling:** clear visuals linked to a narrative (“so what?”).
- **Modeling & segmentation:** interpretable clusters tied to marketing actions.
- **From data to decision:** concrete recommendations per segment and KPIs that matter to Commercial/Marketing.
- **Reproducibility:** notebook + raw data; easy to rerun and extend (e.g., RFM, propensity modeling).

---

## Next steps (roadmap)
- Join `sales_data.xlsx` and customer segments to quantify **revenue by segment**.
- Add **RFM analysis** and **propensity‑to‑respond** modeling for targeted campaigns.
- Build a lightweight **Tableau/Power BI** dashboard that tracks segment KPIs over time.

---

## Contact
**Dante Shoghanian** — MSBA candidate  
Email/LinkedIn: _add yours here_
