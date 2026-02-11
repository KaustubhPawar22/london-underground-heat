# London Underground Heat Exposure — Infrastructure Analytics Case Study

## Overview

This project evaluates historical temperature data from London Underground lines to support infrastructure decision-making for a pilot air-cooling deployment.

Acting as a policy analyst, I performed end-to-end data validation, exploratory analysis, and statistical inference to determine whether meaningful temperature differences exist between the Bakerloo and Central lines — two of the hottest deep-level routes.

The goal was not only to test statistical differences, but to translate results into practical recommendations for transport planners.

The dataset is sourced from Kaggle (compiled from TfL monitoring reports) and is used here for portfolio demonstration.

---

## Key Business Questions

- Which Underground lines experience the highest sustained temperatures?
- Is Bakerloo meaningfully warmer than Central?
- Does this difference persist during peak summer months?
- Where should a pilot air-cooling system be deployed for maximum impact?

---

## Project Structure

london-underground-heat/  
│  
├ data/  
│ └ underground.csv  
│  
├ notebooks/  
│ └ London_Underground_Heat_Exposure_FINAL.Rmd  
│  
└ README.md  


---

## Methodology

### Data Engineering
- Explicit missing-value handling
- Statistical outlier detection using the 1.5×IQR method
- Domain validation of temperature ranges
- Month ordering for seasonal consistency

### Analysis
- Descriptive statistics by line (mean, SD, min, max)
- Distribution diagnostics
- Removal of sub-surface lines per project brief
- Welch’s two-sample t-tests:
  - Annual comparison
  - Summer-only comparison (May–August)
- Effect size calculation (Cohen’s d)

### Decision Framework
- Statistical significance vs practical significance
- Infrastructure-level interpretation
- Executive recommendation with limitations

---

## Key Findings

- Bakerloo and Central lines exhibit the highest sustained temperatures.
- Annual mean difference ≈ **0.7°C** (statistically significant but practically modest).
- Effect size is small (Cohen’s d = 0.26).
- During summer months, no statistically significant difference exists.

### Strategic Insight

Temperature variation appears structurally driven (tunnel depth, ventilation, rolling stock heat retention) rather than isolated to a single route.

---

## Recommendation

While Bakerloo may serve as a reasonable pilot location due to marginally higher annual temperatures, meaningful passenger impact will likely require broader multi-line intervention.

---

## Limitations

- Monthly averages mask short-term heat spikes
- Passenger density not modelled
- Station-level variation excluded
- Observations are longitudinal (mild independence violation)

---

## Skills Demonstrated

- Data validation & anomaly detection (IQR filtering)
- Exploratory data analysis
- Statistical inference (Welch t-tests)
- Effect size interpretation
- Business translation of analytics
- Infrastructure decision support

---

## Author

Kaustubh Pawar  
Portfolio: https://kaustubhpawar.com


