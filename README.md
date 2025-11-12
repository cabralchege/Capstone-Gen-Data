# The Resilience & Reliability Analyst: A Data Story on Kenya's Energy Future
## Project Description

In recent years, Kenya has faced recurring challenges with **load shedding**, impacting economic stability and daily life. This project moves beyond the headlines to find the data-driven truth. It analyzes over two decades (2000-2024) of Kenya's electricity data to answer a critical question: **Why does this keep happening, and is our national strategy to fix it working?**

This analysis is presented as a data story, walking through a 6-chart narrative that diagnoses the historical problem, analyzes the current strategy, and delivers a final, data-driven verdict on the future of Kenya's energy security.

**View the final deployed project here:** `[[LINK TO DEPLOYED WEBSITE](https://kenya-power-story.lovable.app/)]`

---

Load shedding is not just an inconvenience; it's a critical threat to Kenya's economy and daily life. This project is a direct response to this recurring crisis. It analyzes over two decades (2000-2024) of Kenya's electricity data to move past the headlines and answer the *real* questions: 

* **Why does this keep happening?** * **Is this a new, sudden problem, or a long-term structural failure?**
* **Is our national strategy to fix it *actually working*?**

This analysis is presented as a "scrollytelling" data story, walking through a 6-chart narrative that diagnoses the root cause of our grid vulnerability and delivers a final verdict on the solutions being deployed.

**View the final deployed project here:** `[LINK TO YOUR LOVABLE WEBSITE]`

---

## Problem Statements

This analysis was built to test two central hypotheses about the load shedding crisis:

* **H1:** The root cause of load shedding is not a recent failure, but a long-term **structural vulnerability**. This vulnerability is a costly over-reliance on rain-fed hydropower, leading to a "Drought Penalty."
* **H2:** The national strategy to pivot to Geothermal and Wind is the correct solution, but **it is not being implemented fast enough** to close the gap between rising demand and new generation, leading to continued shortfalls.

## Project Objectives

To test these hypotheses, the project had three main objectives:

1.  To **quantify** the relationship between load shedding (grid deficits) and its historical root cause (the "Drought Penalty").
2.  To **evaluate** the effectiveness of the "Great Rebalancing" (the national pivot to Geothermal and Wind) as a strategic solution.
3.  To **deliver** a final, data-driven verdict on whether the current pace of new generation is sufficient to end load shedding in the near future.

## Data Sources

The analysis was built on two primary datasets, both sourced from **Ember**'s aggregated energy data:

1.  **Kenya Electricity Generation (2000-2024):** Annual TWh generation, broken down by source (hydro, fossil, geothermal, wind, solar, etc.).
2.  **Kenya Electricity Demand (2000-2024):** Annual TWh total national demand.

## Methodology & ETL

The raw data was processed in Tableau to create a clean, analysis-ready dataset.

1.  **Extract:** Loaded the raw energy data.
2.  **Transform:**
    * **Filtered** the data to include only `country = "Kenya"` and `year >= 2000`.
    * **Engineered new features** (calculated fields) critical for the analysis:
        * `Grid Surplus/Deficit`: `SUM(electricity_generation) - SUM(electricity_demand)`. This is our primary proxy for "load shedding."
        * `% Share`: (e.g., `SUM(hydro_electricity) / SUM(electricity_generation)`)
        * `Total New Renewables`: `SUM(geothermal) + SUM(wind) + SUM(solar)`
3.  **Load:** Used this transformed dataset as the single source for all visualizations.

---

## The Data Story: A 6-Chart Narrative

The final project tells a story in six charts, each answering a specific question about the load shedding crisis.

### 1. The Growing Challenge: Kenya's Race for Power
* **Insight:** This chart frames the core conflict that *enables* load shedding. It shows the dangerously thin margin between what we need (demand) and what we make (generation).

### 2. The Load Shedding Gap (Grid Surplus/Deficit)
* **Insight:** This *is* the load shedding chart. It quantifies the problem, showing the actual TWh deficit (red bars) that citizens experience as blackouts. It proves this is a recurring, structural issue, not a new one.

### 3. The Historical Culprit: The "Drought Penalty"
* **Insight:** This chart diagnoses the *historical cause* of the deficits. The "X" pattern proves that for decades, a dip in rain (blue line) directly caused a costly and polluting spike in fossil fuels (red line).

### 4. The Great Rebalancing: Kenya's Energy Mix
* **Insight:** This chart shows the *strategic response* to the problem from Chart 3. The "crossover" in 2015 is the moment Kenya's strategy to fight the Drought Penalty (by building Geothermal) went into full effect.

### 5. The New Engines of Growth: Geothermal vs. Wind
* **Insight:** This chart isolates the *solutions*. It shows the two "heroes" (Geothermal and Wind) that are being deployed to kill the red bars from Chart 2.

### 6. The Verdict: The Gap Persists
* **Insight:** This final side-by-side view delivers the verdict. It compares the problem (the red deficit bars) to the solution (the green renewable bars). The conclusion is clear: the solution is not yet big enough.

## Key Takeaways

* **Load Shedding is Structural:** The crisis is not new. The data proves it is a structural deficit, proven by 20+ years of recurring generation gaps.
* **The Root Cause is the "Drought Penalty":** The problem has been a costly and predictable over-reliance on rain-fed hydropower.
* **The Strategy is Correct:** The "Great Rebalancing"—Kenya's pivot to Geothermal and Wind—is clearly the right solution.
* **The Final Verdict: We Have a Speed Problem.** The 2024 data is clear: our new renewable engines are **not yet growing fast enough** to close the gap. To end load shedding, we must build faster.

## Tools Used

* **Data Transformation:** Tableau, Microsoft Excel
* **Data Visualization:** Tableau Public
* **Deployment:** Lovable (for the portfolio website)
