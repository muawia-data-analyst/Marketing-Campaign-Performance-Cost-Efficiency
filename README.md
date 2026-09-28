# Marketing Campaign Performance & Cost Efficiency Analysis

## Overview
A Marketing Data Analyst project analyzing 200,000 marketing campaign records to evaluate performance across channels, campaign types, audiences, and geography. It applies correct weighting (spend-weighted and click-weighted metrics instead of naive averages) and then examines six independent dimensions to see whether any of them drives ROI. Built in Tableau, covering the full lifecycle from data validation and calculated field design to two interactive dashboards and an evidence based conclusion.

## Tools Used
Tableau · Calculated Fields · Parameters · Weighted KPI Aggregation

## Business Context
Marketing and strategy teams constantly ask which channel, audience, or campaign type actually drives return. Most reporting answers this with simple averages, which can be misleading when campaign sizes vary widely. This project simulates that decision-making need across a 200,000-record dataset spanning a full year (2021), 5 companies, 6 channels, and 5 customer segments.

## Key Metrics Designed
* **Weighted ROI** — `SUM(ROI × Acquisition Cost) / SUM(Acquisition Cost)`, weighting each campaign's contribution by spend rather than treating every campaign equally
* **Weighted Conversion Rate** — `SUM(Conversion Rate × Clicks) / SUM(Clicks)`, weighted by traffic volume
* **Overall CTR** — `SUM(Clicks) / SUM(Impressions)`, calculated at the aggregate level rather than averaging pre computed rates
* **Cost vs. ROI** — every campaign plotted individually (200,000 points) to check whether spend level relates to return

## What This Project Includes
* Data validation and field type correction on a 200,000 record dataset (16 fields, full 2021 calendar year)
* Design decision: replaced naive `AVG()` aggregations with spend weighted and click-weighted calculated fields, since simple averages distort results across campaigns of very different scale
* **Dashboard 1 — Performance Overview:** 4 headline KPI cards (Total Campaigns, Total Spend, Overall CTR, Weighted ROI) plus Channel and Campaign Type performance comparisons
* **Dashboard 2 — Audience, Geography & Cost Efficiency:** Target Audience × Customer Segment heatmap, Location × Channel engagement analysis, and a 200,000-point cost vs. ROI scatter plot
* Interactive parameter control on the Audience × Segment heatmap, letting viewers switch between Weighted ROI, Weighted Conversion Rate, and Average Engagement Score in a single view
* Systematic exploration across 6 dimensions: Channel, Campaign Type, Audience × Segment, Location × Channel, Engagement Score, and Acquisition Cost vs. ROI
* **Finding:** ROI, conversion rate, and engagement are essentially flat across every dimension tested (ROI stays within roughly 4.97–5.04 across channels, campaign types, and audience segments), and the cost vs. ROI scatter shows no visible relationship. No dimension in this dataset meaningfully drives ROI, which points to drivers not captured in these fields (creative, timing, competitive context).

## Files in This Repository
* `Marketing_Campaign_Performance_Cost_Efficiency.twbx` — packaged Tableau workbook (both dashboards)
* `marketing_campaign_dataset.xlsx` — source dataset

## How to View
Download the `.twbx` file and open it in [Tableau Public](https://public.tableau.com/) or [Tableau Desktop](https://www.tableau.com/products/desktop) (both free) to interact with both dashboards.
