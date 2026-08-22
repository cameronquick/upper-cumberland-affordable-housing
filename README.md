# Upper Cumberland Affordable Housing Gap Analysis

A data analytics capstone project measuring the gap between vulnerable low-income populations and available federally subsidized housing across the 14 counties of the Upper Cumberland.

## Overview

This project combines U.S. Census/ACS data, HUD's public housing inventories, and THDA housing needs data to identify where HUD Section 202/811 housing (built specifically for low-income seniors and people with disabilities) is most critically under-supplied, relative to the population that needs it. The output is an interactive Tableau dashboard intended to help UCDD leadership prioritize future THDA, HUD, and USDA grant applications.

## Research Questions

1. How are existing HUD-subsidized units distributed across the 14 UCDD counties relative to total regional population?
2. Are regional housing shortages more strongly correlated with concentrations of elderly populations, disability rates, or extreme poverty levels?
3. Which specific counties exhibit the highest net housing deficit, and how does local rent burden amplify this vulnerability?
4. How can UCDD prioritize future grant applications to maximize impact in the most severely underserved counties?

## Data Sources

| Source | Provides |
|---|---|
| U.S. Census/ACS 2020–2024 5-Year Estimates (S0101, S1810, S1701) | Age, disability, and poverty data by county |
| HUD Picture of Subsidized Households | County-level 202/811 unit summaries |
| HUD Multifamily Properties (Assisted) | Property-level location and unit data |
| THDA Housing Needs Assessment | Rent/owner cost burden by county |


```

## Key Methodology Notes

- Uses ACS **5-Year** estimates, since 1-Year estimates aren't published for counties under 65,000 population (all 14 UCDD counties fall below this threshold)
- One manual data correction: Pickett County's unit count includes Hillcrest Apartments, which HUD's automated database doesn't flag as 202/811, but which the property's operator (UCDD/CRDC) describes as serving both eligible populations — documented in full in `docs/methodology_notes.md`
- "202/811 units" and "other HUD-assisted housing" are tracked as separate metrics, since combining them would obscure which counties have population-specific supply versus general-purpose subsidized housing
- Eligible population estimates use Census age-bracket data to avoid double-counting residents who are both elderly and disabled

Full methodology, limitations, and anticipated Q&A are in [`docs/methodology_notes.md`](docs/methodology_notes.md).

## Known Limitations

- 14 counties is a small sample; correlation findings should be read as directional, not statistically definitive
- Two independent HUD sources (county-summary vs. property-level) don't fully agree on unit counts in every county
- Rent burden reflects the standard 30%+ cost-burden threshold; no distinct "severe" (50%+) burden field exists for renters in the source data
