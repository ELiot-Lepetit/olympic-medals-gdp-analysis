# Olympic Medal Performance & Economic Power — Econometric Analysis

## Overview

This project investigates the extent to which a country's economic power 
is reflected in its performance at the Olympic Games, using data from the 
**2016 Rio Summer Olympics**.

The analysis is built around an OLS framework and identifies the 
**number of athletes** as the key mediating channel between GDP and medal 
count. Results are robust to the inclusion of gender, population, sport 
expenditure, and time devoted to sport per week.

> **Group project** — Raphaëlle Dridi, Carla Le Durand, Eliot Lepetit  
> CPES Economics — Université PSL, 2023

---

## Research Question

> *To what extent is the economic power of a country reflected through 
> the Olympic Games?*

---

## Main Findings

- A **1% increase in GDP** leads to a 0.017 increase in medals won 
  (i.e., GDP must increase by ~75% to win one extra medal).
- The effect is **mediated by delegation size**: GDP → number of athletes 
  → number of medals.
- The baseline coefficient is **robust** to adding gender, population, 
  sport expenditure and hours of sport per week as controls.
- **Heterogeneity** by sport type: the GDP effect is stronger for 
  individual sports (1 extra medal per +57% GDP) than collective sports 
  (+103% GDP).

---

## Methodology

- **Strategy:** OLS regression with progressive controls
- **Dependent variable:** Number of medals won per country (2016)
- **Key independent variable:** Log GDP (World Bank, 2016)
- **Mediation analysis:** Number of athletes as mediating variable
- **Robustness checks:** 6 nested specifications
- **Heterogeneity analysis:** Interaction term — GDP × sport category 
  (individual vs. collective)
- **Tool:** R (RMarkdown), rendered as HTML report

---

## Repository Structure
```text
├── Olympic_Games_Final_Report_CPES-2023.Rmd   # Full analysis (R Markdown)
├── Olympic-Games-Final-Report-CPES-2023.html  # Rendered HTML report
└── Data/
    ├── GDP2016.xlsx              # GDP by country, 2016 (World Bank)
    ├── GDP2016PERCAPITA.xlsx     # GDP per capita, 2016 (World Bank)
    ├── Population2016.xlsx       # Population by country, 2016 (World Bank)
    ├── Loisirs.xlsx              # Public leisure & culture expenditure (IMF)
    ├── TimeExercicesperweek.xlsx # Hours of sport per week by country (Ipsos, 2021)
    └── Sportscollectifs.xlsx     # List of collective sports (manual classification)
# athlete_events.csv is too large to be included
```

---

## Data Sources

| File | Source | Access |
|---|---|---|
| `athlete_events.csv` | [Kaggle — 120 years of Olympic history](https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results) | Public |
| `GDP2016.xlsx` | World Bank | Public |
| `GDP2016PERCAPITA.xlsx` | World Bank | Public |
| `Population2016.xlsx` | World Bank | Public |
| `Loisirs.xlsx` | IMF | Public |
| `TimeExercicesperweek.xlsx` | Ipsos — *Global Views on Exercise*, July 2021 | Public |

---

## Requirements

- **R** (developed on R 4.x)
- Key packages: `tidyverse`, `ggplot2`, `stargazer`, `prettydoc`  
  *(install via `install.packages()` if needed)*

---

## Authors

**Raphaëlle Dridi, Carla Le Durand, Eliot Lepetit**  
CPES — Université PSL, 2023 
