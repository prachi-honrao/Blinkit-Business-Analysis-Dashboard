# 🛒 Blinkit Business Dashboard (Power BI)

An interactive Power BI dashboard that analyzes **product performance, outlet operations, sales trends and customer satisfaction** for Blinkit, one of India's leading quick-commerce companies.

---

## 📌 Business Problem

Blinkit's management identified these challenges:

- Some product categories underperform despite high demand
- Outlet performance varies across Tier 1, Tier 2 and Tier 3 cities
- Sales are affected by item visibility and fat content labeling
- Customer satisfaction and repeat purchases need close monitoring

## 🛠 Tools & Skills

`Power BI` · `Power Query` · `DAX` · `Data Modeling (Star Schema)` · `Data Cleaning` · `Data Visualization`

---

## 🗂 Dataset

Blinkit Grocery dataset with **8,523 sales records**, 16 item types, 10 outlets and 3 city tiers.

| Category | Columns |
|---|---|
| Item Details | Item Identifier, Item Type, Item Fat Content, Item Weight, Item Visibility |
| Sales Details | Sales, Rating, Outlet Identifier |
| Outlet Details | Outlet Establishment Year, Outlet Location Type (Tier 1/2/3), Outlet Size, Outlet Type |

## 🔧 Data Cleaning & Transformation (Power Query)

- Standardized inconsistent fat content labels (`LF`, `low fat` → **Low Fat**; `reg` → **Regular**)
- Handled 1,463 missing Item Weight values (excluded from Sales per Kg)
- Set correct data types for numeric and categorical columns
- Split the raw file into lookup tables: **Items, Item Content, Outlet Info, Outlet Location, Cities**
- Created calculated columns: **Sales per Kg**, **Years of Operation**

## 🧩 Data Model (Star Schema)

- **Fact table:** Sales (`BlinkIT_Grocery_Data`)
- **Dimension tables:** Items, Item Content, Outlet Info, Outlet Location, Cities
- **Relationships:** many-to-one from the fact table to each dimension

## 📐 DAX Measures

| Measure | Purpose |
|---|---|
| Total Sales | Total revenue across all outlets |
| Average Sales per Outlet | Average outlet performance |
| Average Item Rating (CSAT) | Overall customer satisfaction |
| Sales per Kg | Revenue relative to item weight |
| Average Years of Operation | Average outlet age |
| Sales by Fat Content / Tier / Outlet Type | Segment comparisons |
| Top 10 Items | Highest-selling items with ratings |

## 📊 Dashboard Features

- **KPI cards:** Total Sales, Avg Sales per Outlet, Avg Rating, Sales per Kg, Avg Years of Operation
- **Visuals:** bar/column charts, line chart, donut chart, scatter (visibility vs sales), Top 10 matrix
- **Slicers:** Tier, Outlet Type, Item Type, Fat Content
- **Drill-through:** Tier → Outlet Type → Outlet → Item
- **Conditional formatting:** highlights outlets with below-average sales

---

## 📈 Key Results

| KPI | Value |
|---|---|
| Total Sales | **1.20M** |
| Average Sales per Outlet | **120.2K** |
| Average Rating (CSAT) | **3.97 / 5** |
| Sales per Kg | **10.98** |
| Average Years of Operation | **5.7 years** (reference year 2022) |

> Profit Margin % and Sales vs Target are not included because the dataset has no cost or target data.

## 💡 Key Insights

1. **Top categories:** Fruits & Vegetables (14.8%) and Snack Foods (14.6%) lead, followed by Household (11.3%) and Frozen Foods (9.9%). The top 4 categories make up about 51% of sales.
2. **Fat content:** Low Fat items bring in **64.6%** of sales versus 35.4% for Regular. This is driven by purchase volume, because the average sale value (140.7 vs 141.5) and rating (3.97 vs 3.97) are almost identical.
3. **Outlet type:** Supermarket Type 1, 2 and 3 each average about **131K per outlet**, while Grocery Stores average only **76K (about 42% lower)**.
4. **Tier:** Tier 3 has the highest total sales (472K) only because it has 4 outlets. Per outlet, **Tier 2 leads (131K)**, then Tier 3 (118K) and Tier 1 (112K).
5. **Establishment year:** Outlet age does not drive sales. The 2022 outlet performs as well as the 2012 supermarket, and the two Grocery Stores (2011, 2018) are the weakest.
6. **Item visibility:** Correlation with sales is about **0 (-0.001)**. Baking Goods has above-average visibility but the lowest average sale value (126.4).
7. **Customer satisfaction:** Stable across segments (3.88 to 4.02). Meat rates highest (4.02) and Breads lowest (3.88). About 5% of records are rated below 3.0.

## ✅ Recommendations

- Fix or repurpose Grocery Stores, which sell about 42% less per outlet
- Use the best Tier 2 and Tier 1 supermarkets (OUT035, OUT046, OUT013) as templates for new openings
- Protect availability of the core categories (Fruits & Vegetables, Snacks, Household, Frozen)
- Replace visibility-based promotion with pricing, bundles and A/B-tested offers
- Investigate low ratings in Breads, Hard Drinks, Soft Drinks and low-rated top sellers

📄 Full write-up: [`docs/Business_Insights_Report.pdf`](docs/Business_Insights_Report.pdf)

---

## 📁 Repository Structure

```
Blinkit-Power-BI-Dashboard/
├── README.md
├── data/
│   ├── raw/                  # Original dataset files
│   └── processed/            # Cleaned lookup tables
├── dashboard/
│   ├── Blinkit_Dashboard.pbix
│   └── Blinkit_Business_Dashboard.pdf
├── assets/
│   └── icons/
└── docs/
    ├── Business_Insights_Report.pdf
    └── Project_Brief.pdf
```

## ▶️ How to Open

1. Download `dashboard/Blinkit_Dashboard.pbix`
2. Open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free)
3. If prompted, update the data source paths to the files in `data/`

## 🙋 Author

**Your Name**
[LinkedIn](https://linkedin.com/in/your-profile) · [GitHub](https://github.com/your-username)

*Project completed as part of the Innomatics Technology Hub data analytics program.*
