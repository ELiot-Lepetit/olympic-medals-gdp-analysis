# Olympic Medal Performance & Economic Power — Econometric Analysis

## Overview
This project investigates the relationship between a country's economic resources and its performance at the 2016 Rio Summer Olympic Games.

Using cross-country data, the analysis examines the association between GDP and the number of Olympic medals won. It relies on OLS regression models, progressively introduces additional control variables, explores the role of delegation size, and investigates differences between individual and team sports.

> **Group project** — Raphaëlle Dridi, Carla Le Durand, Eliot Lepetit  
> CPES Economics — Université PSL, 2023

---

## Research Question

> *To what extent is the economic power of a country reflected through 
> the Olympic Games?*

---

## Main Findings

- GDP is positively associated with the number of Olympic medals won across countries in the baseline OLS specification.
- The analysis explores delegation size (number of athletes) as a potential channel linking a country's economic resources to its Olympic performance.
- The positive association is examined across specifications including additional controls such as gender, population, public sport expenditure and time devoted to sport.
- The analysis also explores differences between individual and team sports, with the estimated relationship varying across the two categories.

These findings describe statistical associations in the 2016 Olympic cross-country sample and should not be interpreted as evidence of a causal effect of GDP on medal counts.

---

## Methodology

- **Empirical approach:** Ordinary Least Squares (OLS) regression.
- **Outcome variable:** Number of medals won by each country at the 2016 Rio Summer Olympics.
- **Main explanatory variable:** Country-level GDP in 2016.
- **Additional controls:** Gender, population, public sport expenditure and time devoted to sport per week.
- **Delegation size:** Explored as a potential explanatory channel through additional regression specifications.
- **Robustness checks:** Six nested model specifications.
- **Heterogeneity analysis:** Examination of differences between individual and team sports using an interaction term between GDP and sport category.
- **Tools:** R and R Markdown.

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

---

## Authors

**Raphaëlle Dridi, Carla Le Durand, Eliot Lepetit**  
CPES — Université PSL, 2023 
