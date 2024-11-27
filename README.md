# Post-COVID Commute Analysis

As a Data Visualization Specialist at the Metropolitan Transportation Authority (MTA), my task was to create an interactive dashboard showcasing post-pandemic ridership recovery trends. Using advanced data tools, I transformed complex ridership data into clear, actionable insights to help stakeholders understand recovery patterns across services.

## Executive Summary
- In April 2020, all forms of transportation, except Access-A-Ride and Bridges and Tunnels, experienced a sharp decline, with usage dropping to less than 8% of pre-COVID levels.
- Bridges and Tunnels showed the most resilience, reaching 92% of pre-COVID flow levels within May 2021. After that, it consistently maintained flows at pre-COVID levels, even surpassing them in some months.
- Each year from October to November, there is a noticeable spike in usage for the Staten Island Railway, Metro-North Line, and Long Island Rail Road. This trend highlights the heavy traffic associated with Thanksgiving, as many people travel to visit their families during this time.
- A consistent dip occurs from November to December each year, but in 2022, this dip was even more pronounced and extended into January due to the emergence of the Omicron variant.

![Snapshot of the Dashboard](https://github.com/nuhash-cell/Post-covid-commute-analysis/blob/main/Snapshots/ReportPage.png)

## Dataset
The dataset includes daily passenger flows across seven types of transportation systems over a span of five years, covering the COVID-19 period up to October 2024. It also includes percentages that show how the current flow compares to pre-COVID levels.

## Data Cleaning and Modeling
The data was well-structured from the start, so I didn't need to apply any advanced data cleaning or preprocessing techniques.  
- I created seven calculated columns to capture the pre-pandemic transportation flows, avoiding reliance on quick measures that could slow down visualizations.
- For dates where flows were recorded as zero (e.g., Staten Island Railway), I assumed pre-pandemic flow as zero to ensure valid calculations.

**Formula:**
```python
Pre-COVID Flow = if [Percentage of Pre-COVID Levels] = 0 then 0 else [Total Ridership] / ([Percentage of Pre-COVID Levels] / 100)
```

## Approach
- I designed the visualization with a timeline on the x-axis to highlight fluctuations and trends over time, making it easy to share insights with stakeholders.
- I created custom measures in the columns to enable dynamic filtering via the selection panel, improving user interactivity.
- I added a threshold range (90% to 110%) with markers for lines crossing this range, clearly indicating recovery near or better than pre-COVID levels.

[View the Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiYWMxNjZiMzQtMWYwOC00Yjg2LWEzMjMtNmYyN2U0N2U5MGJiIiwidCI6IjdjNjRkYTk4LTE4NmQtNGNkMC04NDZiLTkyZDQxOGY0YmJkZiIsImMiOjEwfQ%3D%3D)
