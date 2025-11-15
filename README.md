# Business Insight 360 — Power BI Analytics Suite

**Author:** Gaurav Nikam  
**Contact / Portfolio:** [LinkedIn]((https://www.linkedin.com/in/-471-gaurav-nikam)) | Email: gauravnikam471@gmail.com.in

**Live demo:**  
👉 [Open the interactive report in Power BI Service](https://app.powerbi.com/view?r=eyJrIjoiZDBjNjc0YjctZGZmMy00MDE3LTkzNWQtNDVhOGJkNmEyMDg3IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

---

## Project summary

**Business Insight 360** is a full-scale, enterprise-grade Power BI solution designed to give leadership a consolidated view of performance across **Finance, Sales, Marketing, Supply Chain,** and **Executive** operations.  
It demonstrates end-to-end BI development: data ingestion and cleansing, star-schema modelling, advanced DAX, parameterization, and a polished UX with bookmarks, tooltips and a custom JSON theme.



---

## Table of contents

- [Why this project](#why-this-project)  
- [What you’ll find in this repo](#what-youll-find-in-this-repo)  
- [Detailed page-by-page walkthrough](#detailed-page-by-page-walkthrough)  
- [Data model & architecture](#data-model--architecture)    
- [What I learned — skills & outcomes](#what-i-learned---skills--outcomes)  


---

## Why this project

- Demonstrates building a complete **enterprise reporting product**, not just a single dashboard.  
- Uses real-world reporting patterns: star schema, utility tables, parameterized views, and performance-aware DAX.  
- UX-first design: navigation tiles, a left-side filters panel, pop-up support panel, tooltip pages, and a custom theme.  
- Practical for interviews — shows modeling, DAX proficiency, and product thinking.

---

## What you’ll find in this repo

- `README.md` — this file (you’re reading it).    
- `gifs/` — animated previews of pages (small web-friendly GIFs).   
- `dashboard.pbix` *(optional: see Hosting & File Size)*

---

## Detailed page-by-page walkthrough

> Below each page I list the business purpose, key visuals, and what I implemented technically.

### Home (Landing)
**Purpose:** Launchpad — quick navigation to each functional area.  
**Key visuals & elements:** Logo, last refresh timestamp, 6 navigation tiles (Finance, Sales, Marketing, Supply Chain, Executive, Help).  
**Implementation notes:** Built using bookmarks & button actions. Clean layout for quick demos.

[Home Page](https://github.com/GauravN471/Business_Insight_360/blob/main/Home-ezgif..gif)
---

### Finance View
**Purpose:** Full P&L analysis and financial KPIs for decision makers.  
**Key visuals:**  
- KPI cards: Net Sales, Gross Margin %, Net Profit %, Forecast Accuracy %.  
- Net Sales trend area + contribution chart.  
- Full P&L table (Gross Sales → Net Profit) with drillable rows.  
- Top/Bottom Products & Customers matrix.  
**Technical highlights:**  
- P&L rows modelled as utility table.  
- Benchmarks (LY vs Target) controlled via parameter `Set BM`.  
- Conditional formatting via DAX measures (color bars & arrows).

[Finance Page](https://github.com/GauravN471/Business_Insight_360/blob/main/FinanceView-ezgif.gif)

---

### Sales View
**Purpose:** Customer & Product performance and contribution analysis.  
**Key visuals:** Bubble/scatter for NS vs GM%, contribution donut, product/customer matrices.  
**Technical highlights:** Dynamic sorting, measure-driven labels, field parameter to switch dimension.

[Sales Page](https://github.com/GauravN471/Business_Insight_360/blob/main/SalesView-ezgif.gif)
---

### Marketing View
**Purpose:** Segment and category performance; marketing contribution.  
**Key visuals:** Bubble charts, market-share visuals, segment tables.  
**Technical highlights:** Field parameters for axis switching; segment-level conditional rules.

[Marketing Page](https://github.com/GauravN471/Business_Insight_360/blob/main/Marketingview-.gif)
---

### Supply Chain View
**Purpose:** Forecast accuracy and operational error analysis.  
**Key visuals:** Combo chart (Net Error bars + Forecast Accuracy line), error trend, product/customer accuracy list.  
**Technical highlights:** Forecast accuracy measures (`ABS Error`, `Forecast Accuracy %`, `Forecast Accuracy Variance`), and conditional thresholds for flags.

[Supply Chain Page](https://github.com/GauravN471/Business_Insight_360/blob/main/Supplychainview-ezgif..gif)
---

### Executive View
**Purpose:** One-page summary for executives with drill-down ability.  
**Key visuals:** High level KPIs, trend sparkline, top customers & products, region summary.  
**Technical highlights:** Consolidates measures from other pages; uses primary & secondary parameters for flexible views.

[Executive Page](https://github.com/GauravN471/Business_Insight_360/blob/main/ExecutiveView-ezgif.gif)
---

## Data model & architecture

**Model type:** Star schema with dimensions and 3 core facts.  
**Dimensions:** `dim_date`, `dim_product`, `dim_customer`, `dim_market`.  
**Facts:** `fact_sales_monthly`, `fact_forecast_monthly`, `fact_actual_estimates`.  
**Supporting facts:** manufacturing & cost tables, invoice deductions, last sales helper tables.  
**Other artifacts:** `Key Measures` (folder/table), `Set BM` (benchmark control), `P&L rows` utility table.  

**Notes:**  
- Relationships configured to keep filter flow logical and performance friendly.  
- Date table is the single source of time intelligence.

---

# What I Learned — Skills & Outcomes

### 📌 Business & Analytical Learning
- P&L structure (Gross Sales → Net Profit)  
- Forecasting concepts: Error %, Net Error, Forecast Accuracy  
- Customer/Product segmentation  
- Market performance & category-level insights  

### 📌 Power BI Modeling
- Star Schema design  
- Utility tables (P&L Rows, Set BM, Measure tables)  
- Managing granular fact tables  
- Optimizing relationships  

### 📌 DAX (Advanced)
- Dynamic benchmarks (LY / Target)  
- Dynamic titles & labels  
- Growth %, variances, YoY calculations  
- Conditional formatting measures  
- Parameter-driven DAX logic  

### 📌 Power Query (M)
- Merging fact & cost tables  
- Cleaning raw Excel data  
- Unpivoting P&L structures  
- Removing absolute file paths  
- Type handling & query grouping  

### 📌 UX & UI Design
- Custom JSON theme  
- Bookmark-based navigation  
- Slide-in support panel  
- Tooltip pages  
- Symmetric layout design  
- Professional slicer panel  

### 📌 Parameters & Interactivity
- Field parameters for axis switching  
- Metric switching (e.g., Customer/Product)  
- dual-parameter logic for executive view  

---

