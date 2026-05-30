# Task 2 — Customer Retention & Churn Analysis

**Author:** Elethu Mahlangeni
---
## Overview
This project analyses a telecom customer dataset to identify churn drivers, segment high-risk customers, and produce actionable retention recommendations. The deliverable is a Power BI dashboard backed by Python-generated aggregation tables.
---
## Files
| File | Description |
|------|-------------|
| `churn_analysis.ipynb` | Full Python analysis notebook |
| `Telco Churn Analysis.pbix` | Power BI dashboard file |
| `Task 2-DS.pdf` | Dashboard export (PDF) |
---
## How to Use
- **Power BI dashboard:** Open `Telco Churn Analysis.pbix` in Power BI Desktop.
- **Python notebook:** Open `churn_analysis.ipynb` in Jupyter or VS Code to re-run the analysis.
- **PDF export:** Open `Task 2-DS.pdf` for a static view without Power BI installed.
---
## Key Findings

| KPI | Value |
|-----|-------|
| Total Customers | 7,043 |
| Churn Rate | **26.54%** |
| Revenue Lost to Churn | **$2,862,927** |
| Monthly Revenue at Risk | $139,131 |
| Avg Tenure — Churned | 18 months |
| Avg Tenure — Retained | 37.6 months |

**Churn by contract type**

| Contract | Churn Rate |
|----------|-----------|
| Month-to-month | **42.71%** |
| One year | 11.27% |
| Two year | 2.83% |

**Churn by internet service**

| Service | Churn Rate |
|---------|-----------|
| Fiber optic | **41.89%** |
| DSL | 18.96% |
| No internet | 7.40% |

**Churn by payment method**

| Method | Churn Rate |
|--------|-----------|
| Electronic check | **45.29%** |
| Mailed check | 19.11% |
| Bank transfer (auto) | 16.71% |
| Credit card (auto) | 15.24% |

**First-year customers churn at 47.44%** — nearly half leave within 12 months.

---

## Top Recommendations

1. **Convert month-to-month customers to annual contracts** — the single biggest lever (42.71% → 2.83% churn rate)
2. **Investigate Fiber Optic quality issues** — 41.89% churn suggests a service or pricing problem
3. **Offer incentives to switch off electronic check** — 45.29% churn vs ~16% for auto-pay methods
4. **Prioritise onboarding in the first 12 months** — 47.44% churn in year one; a dedicated retention programme here pays outsized returns
5. **Target high-value at-risk customers first** — $139K monthly revenue at risk; segment by charge level before outreach

---

## Data Cleaning Summary

| Action | Detail |
|--------|--------|
| Source rows | 7,043 |
| TotalCharges converted | Blank strings → numeric |
| Churn encoded | Yes/No → 1/0 |
| Revenue column added | `MonthlyCharges × Tenure` |
| Tenure bands created | 0–12, 13–24, 25–36, 37–48, 49–60, 61–72 months |
