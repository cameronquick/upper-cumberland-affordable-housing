# Upper Cumberland Affordable Housing Gap Analysis

An analytical exploration and interactive dashboard examining the affordable housing supply and demand gap across the Upper Cumberland in Middle Tennessee. 

This project combines demographic, income, and housing data from the **U.S. Census Bureau (ACS)**, **HUD**, and **THDA** to analyze regional shortages in subsidized housing, specifically focusing on **Section 202** (Supportive Housing for the Elderly) and **Section 811** (Supportive Housing for Persons with Disabilities) programs.

---

## Key Features

* **Supply vs. Demand Analysis:** Quantifies subsidized housing inventory against vulnerable populations across all 14 UCDD counties.
* **Cost-Burden Metrics:** Evaluates low-income renter cost-burden rates across Area Median Income (AMI) tiers ($\le 30\%$, $30-50\%$, and $50-80\%$ AMI).
* **Predictive Insights:** Explores correlations between county disability/poverty rates and housing shortages.
* **Interactive Dashboard:** Built in Tableau, allowing users to toggle between raw unit counts and standardized rates per 1,000 seniors, complete with interactive property-level maps.

---

## Tools & Data Sources

* **Tools:** Python (`pandas`, `numpy`), Tableau Desktop
* **Data Sources:**
  * **U.S. Census Bureau (ACS 5-Year Estimates):** Demographics, disability, poverty, and cost-burden metrics
  * **U.S. Department of Housing and Urban Development (HUD):** Section 202/811 and assisted housing property locations
  * **Tennessee Housing Development Agency (THDA):** Regional housing figures

