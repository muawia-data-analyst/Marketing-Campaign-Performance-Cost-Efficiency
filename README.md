# Marketing Campaign Performance & Cost Efficiency Analysis

## Overview
A Business/Marketing Data Analyst project analyzing 200,000 marketing campaign records to evaluate performance across channels, campaign types, audiences, and geography, then applying correct statistical methodology (weighted metrics, not naive averages) to test whether any single dimension actually predicts ROI. Built using Tableau, covering the full analytical lifecycle from calculated field design through hypothesis testing to a defensible, evidence-based conclusion.

## Tools Used
Tableau Public · Calculated Fields · LOD-style Aggregation Logic

## Business Context
Marketing and strategy teams constantly face the question: *which channel, audience, or campaign type actually drives return?* Most reporting answers this with simple averages which can be misleading when campaign sizes vary widely. This project simulates that exact decision-making need across a 200,000 record dataset spanning a full year (2021), 5 companies, 6 channels, and 5 customer segments.

## Key Metrics Designed
* **Weighted ROI** — `SUM(ROI × Acquisition Cost) / SUM(Acquisition Cost)`, correctly weighting each campaign's contribution by spend rather than treating every campaign equally
* **Weighted Conversion Rate** — `SUM(Conversion Rate × Clicks) / SUM(Clicks)`, weighted by traffic volume
* **Overall CTR** — `SUM(Clicks) / SUM(Impressions)`, calculated at the aggregate level rather than averaging pre-computed rates
* **Cost Efficiency** — ROI evaluated directly against Acquisition Cost per campaign, to separate expensive but effective spend from wasteful spend

## What This Project Includes
* Data validation and field type correction on a 200,000 record dataset (16 fields, full 2021 calendar year)
* Design decision: replaced naive `AVG()` aggregations with spend weighted and click weighted calculated fields, since simple averages would distort results across campaigns of very different scale
* **Dashboard 1 — Performance Overview:** 4 headline KPI cards (Total Campaigns, Total Spend, Overall CTR, Weighted ROI) plus Channel and Campaign Type performance comparisons
* **Dashboard 2 — Audience, Geography & Cost Efficiency:** Target Audience × Customer Segment heatmap, Location × Channel engagement analysis, and a 200,000 point cost vs ROI scatter plot
* Systematic hypothesis testing across 6 independent dimensions Channel, Campaign Type, Audience×Segment, Location×Channel, Engagement Score, and Acquisition Cost vs. ROI directly
* **Finding:** no single dimension tested significantly predicts ROI in this dataset a conclusion reached only after correctly weighting every metric and testing it from multiple independent angles, not assumed from a single chart

## Files in This Repository
* `Marketing_Campaign_Performance_Cost_Efficiency.twbx` — packaged Tableau workbook (both dashboards)
* `marketing_campaign_dataset.xlsx` — source dataset

## How to View
Download the `.twbx` file and open it in [Tableau Public](https://public.tableau.com/) or [Tableau Desktop](https://www.tableau.com/products/desktop) (both free) to interact with both dashboards.
