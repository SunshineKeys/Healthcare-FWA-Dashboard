# Healthcare FWA Detection Dashboard
### Pharmacy Claims — Fraud, Waste & Abuse Detection | Power BI

---

## Overview

This Power BI dashboard analyzes pharmacy claims data to identify patterns of fraud, waste, and abuse (FWA) across a simulated healthcare dataset of 500 claims spanning multiple plan types, drug categories, and patient populations.

Built as part of an ongoing healthcare data analytics portfolio demonstrating domain expertise in pharmacy claims, Medicaid operations, and data visualization.

---

## Dashboard Features

### KPI Cards
- **Total Cost** — aggregate spend across all filtered claims
- **Overall Denial Rate %** — percentage of claims denied, dynamically calculated across all claim statuses
- **High Risk Claims** — count of claims flagged for elevated risk

### Visualizations
- **Denial Rate by Drug (%)** — horizontal bar chart ranking drugs by denial rate to surface potential FWA patterns
- **Total Cost by Therapeutic Category** — treemap showing cost concentration across drug categories (Addiction, Cardiovascular, Oncology, etc.)
- **Top 20 High-Cost Patients** — conditional-formatted table showing patient name, plan type, total cost, claim count, and high-risk claim flags

### Interactive Slicers
- **Filter by Plan Type** — Commercial HMO, Commercial PPO, Medicaid, Medicare Advantage, Medicare Part D
- **Filter by Claim Status** — Denied, Paid, Pending, Reversed

---

## Technical Details

**Tool:** Microsoft Power BI Desktop  
**Data:** Simulated pharmacy claims dataset (500 claims, 4 relational tables)  
**DAX Measures:**
- `Denial Rate %` — DIVIDE with ALL() context modifier to calculate denial rate independent of claim status slicer
- `High Risk Claims` — conditional count flagging elevated-cost outliers
- `Total Cost` — aggregate spend with filter context

**Tables:**
- `pharmacy_claims` — core claims data (claim_id, claim_status, drug, cost, patient, pharmacy)
- `patients` — patient demographics and plan type
- `drug_formulary` — drug category and formulary status
- `cost_by_plan_category` — aggregated cost reporting by plan and category

---

## Key Insights (Simulated Data)

- **Naltrexone** has the highest denial rate at ~40%, suggesting potential formulary compliance issues
- **Medicare Advantage** patients represent the highest-cost cohort with the most high-risk claims
- **Oncology** and **Cardiovascular** categories show the greatest cost concentration in the therapeutic treemap
- Overall denial rate of ~12% across all plan types

---

## Portfolio Context

This dashboard is Part 2 of an ongoing Power BI portfolio series:

| Project | Description | Status |
|---------|-------------|--------|
| Pharmacy Claims Pipeline | End-to-end Python claims analysis (pandas, 4 relational tables) | ✅ Complete |
| FWA Detection Dashboard | Power BI fraud, waste & abuse detection | ✅ Complete |
| Prior Authorization Analytics | PA approval rates, denial reasons, turnaround times | 🔄 In Progress |

---

## Screenshots

*Screenshots coming soon — see dashboard PDF in repo for full interactive view*

---

## About

Built by **Megan Merrigan** — healthcare data analyst with 6+ years of experience in pharmacy operations, Iowa Medicaid claims processing, and rebate reconciliation.

- 🔗 [LinkedIn](https://linkedin.com/in/megan-merrigan-a824a1265)
- 💻 [GitHub Portfolio](https://github.com/SunshineKeys)
- 📊 [Pharmacy Claims Pipeline](https://github.com/SunshineKeys/Pharmacy-Claims-Pipeline)

*Self-taught. Portfolio-driven. Healthcare domain expertise meets Python and Power BI.*
