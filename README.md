# Blinkit Business Analysis using Power BI

## 📌 Project Overview

This project analyzes Blinkit's grocery sales data using **Microsoft Power BI**. It presents interactive dashboards to explore sales performance, product categories, outlet characteristics, and item ratings.

This is a **group project** developed by **Prachi Honrao** and **Bhakti Atkale**.

## 🎯 Project Objectives

- Analyze sales performance using key performance indicators (KPIs).
- Identify top-performing items and product categories.
- Compare sales across outlet types, sizes, location tiers, and establishment years.
- Explore sales distribution by item fat content.
- Examine the relationship between item visibility and sales.
- Present insights through interactive dashboards.

## 🛠️ Tools and Technologies

- **Microsoft Power BI** — dashboard development and visualization
- **Power Query** — data cleaning and transformation
- **DAX** — calculations and conditional logic
- **CSV and Excel** — data sources

## 📊 Dashboard Pages

### Main Dashboard
![Main Dashboard](assets/Main%20Dashboard.png)

Includes KPI cards, sales by outlet tier and type, sales by establishment year and item type, fat-content distribution, a Top 10 Items by Sales table, and an item visibility-versus-sales scatter plot.

### Outlet Analysis
![Outlet Analysis](assets/Outlet%20Analysis.png)

Compares outlet performance, including sales by location tier and average sales by outlet size, along with key performance indicators.

### Item Analysis
![Item Analysis](assets/Item%20Analysis.png)

Explores item types, item counts, sales, fat-content distribution, average item ratings, and item visibility versus sales.

## 🧹 Data

The repository includes raw and processed data files.

- **Raw Data/** contains the original dataset files.
- **Processed Data/** contains the grocery dataset and supporting tables used for analysis.

Power Query was used to inspect data types, check for missing values and duplicates, and prepare the data for reporting. Refer to the Power BI file for the implemented transformation steps.

## 💡 Business Questions Explored

- What are the overall sales and average item rating?
- Which item types contribute most to sales?
- How do sales vary across outlet types and location tiers?
- How does outlet size relate to average sales?
- Which items are among the top 10 by sales?
- Do items with high visibility always have high sales?

## 🔍 Key Takeaways

- Compare sales performance across item categories and outlet characteristics.
- Identify high-performing items using the Top 10 Items by Sales table.
- Use the visibility-versus-sales scatter plot to spot items with relatively high visibility but lower sales.
- Explore the report interactively using available slicers and visuals.

## 🚀 How to View the Dashboard

1. Download or clone this repository.
2. Open `DashBoard/Blinkit Dashboard.pbix` in **Microsoft Power BI Desktop**.
3. If Power BI prompts for data source paths, point them to the files in `Data/Processed Data/` or the relevant source files used by the report.
4. Refresh the data if required.
5. Explore the Main Dashboard, Outlet Analysis, and Item Analysis pages.

A PDF copy of the dashboard is available at `DashBoard/Blinkit_Business_Dashboard.pdf`. Additional business insights are documented in `docs/Business_Insights_Report.pdf`.

## 📁 Project Structure

```text
Blinkit-Power-BI-Dashboard/
├── assets/
│   ├── Main Dashboard.png
│   ├── Outlet Analysis.png
│   ├── Item Analysis.png
│   └── ... (logos, icons, and background assets)
├── DashBoard/
│   ├── Blinkit Dashboard.pbix
│   └── Blinkit_Business_Dashboard.pdf
├── Data/
│   ├── Processed Data/
│   │   ├── BlinkIT Grocery Data.csv
│   │   ├── Cities.csv
│   │   ├── Items Content.csv
│   │   ├── Items.csv
│   │   ├── Outlet Info.csv
│   │   └── Outlet Location.csv
│   └── Raw Data/
│       ├── BlinkIT Grocery Data.csv
│       └── Original.xlsx
├── docs/
│   └── Business_Insights_Report.pdf
└── README.md
```

## 👥 Team Members

- **Prachi Honrao**
- **Bhakti Atkale**

## 📌 Project Type

**Business Intelligence | Data Analytics | Data Visualization**

---

*Created as a collaborative project to practice data preparation, business analysis, and interactive dashboard development using Power BI.*
