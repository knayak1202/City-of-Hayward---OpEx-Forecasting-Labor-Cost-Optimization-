# City of Hayward: Workforce Cost Optimization (FP&A)

**Goal:** Reduce total labor cost while preserving service levels by sizing the best mix of hiring vs overtime for Police and Fire.

**Result:** Projected **$548k** labor cost savings by addressing a **287%** overtime budget variance for FY 2025–26. Identified Police and Fire as the primary drivers from **20k+** records and selected a **four-scenario** plan that links overtime spend to staffing gaps.

## Highlights
- Driver-based model that links vacancies to overtime and quantifies hire versus OT trade-offs
- Four scenarios evaluated: 25%, 50%, 75%, 100% hiring with residual OT
- Cost bridge from status quo overtime to the recommended mix
- Executive readout with savings, payback, and role-level hiring plan

## Data (de-identified in this repo)
- Overtime transactions (about 20k rows)
- Workforce roster and vacancies
- OT budget by department and role
- Pension and benefits loadings



## Method
1. **Data prep**
   - Normalize roles and departments
   - Join OT entries to vacancy status and time periods
   - Create a crosswalk for role codes across sources
2. **Diagnostics**
   - Concentration analysis to find OT-heavy roles
   - Vacancy versus OT correlation to quantify the driver
   - Baseline cost and run rate
3. **Model**
   - Salary + benefits + pension + residual OT at role level
   - Scenario tables for 25% / 50% / 75% / 100% hiring
   - Sensitivities on wage rates, pension %, and OT multipliers
4. **Outputs**
   - Total cost by scenario versus baseline
   - Cost bridge and savings
   - Per-role hiring plan and expected residual OT hours

## Repository structure
```
/data/           # anonymized samples or schemas
/model/          # Excel model with scenario and sensitivity tabs
/notebooks/      # optional Python checks or visuals
/slides/         # executive summary and charts
/docs/           # assumptions log and methodology notes
```

## How to use
1. Open the Excel model in `/model`.
2. Update **Assumptions** (wage rates, pension loadings, OT multipliers, scenario mix).
3. Refresh queries to recalc scenarios.
4. Review **Scenario Summary** and **Cost Bridge** to select the recommendation.
5. Optional: open the Power BI file to view department and role trends.

## Key FP&A metrics
- Total labor cost versus baseline
- Savings and payback by scenario
- Vacancy rate and OT hours
- Cost per FTE and run rate
- Forecast accuracy for the selected plan

## Results 
- Recommended **75% hiring / 25% OT** as the best balance of savings and coverage
- Projected **$548k** reduction in labor cost and a meaningful drop in overtime reliance
- Clear hiring plan for OT-concentrated roles in Police and Fire

## Tech
- **Excel:** Power Query, PivotTables, scenario and sensitivity tables
- **Power BI:** role and department dashboards
- **Python** : data validations and checks

## Limitations
- Assumes stable service demand
- Does not include recruiting capacity constraints



## Contact
Questions or collaboration requests are welcome. Open an issue or reach out via your GitHub profile.
