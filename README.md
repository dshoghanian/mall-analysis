# Shopping Mall Analytics

Exploratory analysis and insights for a shopping mall dataset, including sales and customer behavior.
This repository contains the analysis notebook and the raw Excel files required to run it.

## What's inside

```
shopping-mall-analytics/
├── LICENSE
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── Mall_Analysis.ipynb
│   ├── sales_data.xlsx
│   ├── shopping_mall_data.xlsx
│   └── customer_data.xlsx
├── data/
│   └── README.md
├── reports/
│   └── README.md
└── src/
    └── __init__.py
```

> The three Excel files are placed in `notebooks/` so that `Mall_Analysis.ipynb` can load them using the existing relative paths (e.g., `pd.read_excel("sales_data.xlsx")`).

## Quickstart

### 1) Create and activate a virtual environment
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux:
source .venv/bin/activate
```

### 2) Install dependencies
```bash
pip install -r requirements.txt
```

### 3) Launch Jupyter and open the notebook
```bash
jupyter lab
```
Then open: `notebooks/Mall_Analysis.ipynb`

## Pushing this project to GitHub

**Option A — GitHub website**
1. Create a new repo named `shopping-mall-analytics` on GitHub.
2. Download the ZIP from your assistant and extract it.
3. In a terminal, run the commands under Option B from inside the extracted folder (or upload via the web UI).

**Option B — Git (CLI)**
```bash
cd shopping-mall-analytics
git init
git add .
git commit -m "Initial commit: project structure, notebook, and data"
# Replace <YOUR-USERNAME> with your GitHub username and set visibility as desired
git branch -M main
git remote add origin https://github.com/<YOUR-USERNAME>/shopping-mall-analytics.git
git push -u origin main
```

> Tip: If any `.xlsx` files ever grow beyond ~100 MB (GitHub's limit per file), set up [Git LFS](https://git-lfs.com) before committing:
> ```bash
> git lfs install
> git lfs track "*.xlsx"
> git add .gitattributes
> ```

## Notes

- `requirements.txt` includes `openpyxl` so `pandas.read_excel` works out of the box.
- If you later refactor paths so the raw files live in `data/raw/`, update the notebook reads accordingly.
- License: MIT (see `LICENSE`).

---

