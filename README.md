# 📊 Sales Forecasting Dashboard — Power BI

A comprehensive, interactive Power BI dashboard designed to track, analyze, and forecast retail sales performance across regions, categories, ship modes, and customer segments using 2019–2021 order data.

---
## 🎬 Dashboard Demo

![Dashboard Demo](https://github.com/29Rajeswari/Sales_Forecasting/assets/200754034/your-video-filename.mp4)

## 📸 Dashboard Preview

### Page 1 — Sales Overview
![Sales Overview](https://raw.githubusercontent.com/29Rajeswari/Sales_Forecasting/main/Sales%20Overview.png)

### Page 2 — Sales Forecasting
![Sales Forecasting](https://raw.githubusercontent.com/29Rajeswari/Sales_Forecasting/main/Sales%20Forecasting.png)

---

## 📁 Repository Structure

```
Sales_Forecasting/
│
├── Sales forecasting..pbix     # Main Power BI report file
├── Sales Overview.png          # Screenshot — Page 1
├── Sales Forecasting.png       # Screenshot — Page 2
└── README.md
```

> 📥 **Download the report:** [Sales forecasting..pbix](https://github.com/29Rajeswari/Sales_Forecasting/raw/refs/heads/main/Sales%20forecasting..pbix)

---

## 🗂️ Dashboard Pages

### Page 1 — Sales Overview

A high-level summary dashboard with key KPIs and category-level breakdowns.

| Section | Visual Type | Description |
|---|---|---|
| KPI Cards | Card | Total Sales (2M), Profit (175K), Avg (23K), Quantity (22K) |
| Sales by State | Map (Bubble) | Geographic distribution of sales across the US |
| Sales by Category | Horizontal Bar | Office Supplies (0.64M), Technology (0.47M), Furniture (0.45M) |
| Sales by Sub-Category | Horizontal Bar | Top 3: Phones (0.20M), Chairs (0.18M), Binders (0.17M) |
| Sales by Month & Year | Area Chart | Year-over-year comparison (2019 vs 2020) |
| Profit by Month & Year | Area Chart | Monthly profit trends across 2019 and 2020 |
| Sales by Ship Mode | Bar Chart | Standard Class (0.33M) leads, followed by Second / First / Same Day |
| Sales by Payment Mode | Donut Chart | Online, Cards, COD — each ~33% |
| Sales by Avg Delivery | Donut Chart | Delivery time distribution |
| Sales by Segment | Donut Chart | Consumer (48%), Corporate (33%), Home Office (19%) |
| Region Filter | Slicer | Central, East, South, West |

---

### Page 2 — Sales Forecasting

A dedicated time-series and forecasting view for deeper temporal analysis.

| Section | Visual Type | Description |
|---|---|---|
| Sum of Sales by Order Date | Area Chart | Daily sales from Jan 2019 to Jan 2021 |
| Sales Forecasting | Line Chart + Forecast Band | Recent trend with 15-day forecast and confidence interval |
| Sales by State | Bar Chart | Top 10 states: California (0.34M), New York (0.19M), Texas (0.12M), etc. |

---

## 📊 Key Metrics at a Glance

| Metric | Value |
|---|---|
| Total Sales | 2,000,000 (2M) |
| Total Profit | 175,000 (175K) |
| Avg Sales | 23,000 (23K) |
| Total Quantity | 22,000 (22K) |
| Top Category | Office Supplies — 0.64M |
| Top Sub-Category | Phones — 0.20M |
| Top Ship Mode | Standard Class — 0.33M |
| Top State | California — 0.34M |
| Top Segment | Consumer — 48% |

---

## 🌍 Regional Filter

The dashboard supports filtering by 4 regions via an interactive slicer:

- **Central**
- **East**
- **South**
- **West**

All visuals on Page 1 update dynamically when a region is selected.

---

## 🔮 Forecasting Methodology

The Sales Forecasting chart (Page 2) uses Power BI's built-in **time-series forecasting** feature:

- **Historical window:** Jan 2019 — Dec 2020
- **Forecast horizon:** ~15 days beyond the last data point
- **Confidence interval:** Shaded band indicating upper and lower bounds
- **Granularity:** Daily order-level aggregation

The forecast is generated natively using Power BI's Analytics pane (exponential smoothing).

---

## 🗃️ Dataset Details

| Field | Description |
|---|---|
| Order Date | Date the order was placed |
| Ship Mode | Standard Class / Second Class / First Class / Same Day |
| Segment | Consumer / Corporate / Home Office |
| State | US state of the customer |
| Region | Central / East / South / West |
| Category | Furniture / Office Supplies / Technology |
| Sub-Category | Phones, Chairs, Binders, etc. |
| Sales | Revenue in USD |
| Profit | Profit in USD |
| Quantity | Number of units ordered |
| Payment Mode | Online / Cards / COD |
| Avg Delivery | Average delivery days |

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Report creation & visualization |
| **Power Query (M)** | Data transformation & cleaning |
| **DAX** | Calculated measures (KPIs, YoY comparisons) |
| **Power BI Analytics Pane** | Built-in time-series forecasting |
| **Bing Maps** | Geographic bubble map for US states |

---

## ⚙️ How to Open the Report

1. **Install Power BI Desktop**
   Download free from [https://powerbi.microsoft.com/desktop](https://powerbi.microsoft.com/desktop)

2. **Clone this repository**
   ```bash
   git clone https://github.com/29Rajeswari/Sales_Forecasting.git
   ```

3. **Open the report file**
   - Launch Power BI Desktop
   - Go to **File → Open** and select `Sales forecasting..pbix`

4. **Refresh data (if needed)**
   - Go to **Home → Transform Data** to update the data source path
   - Click **Refresh** to reload

---

## 📌 Sample DAX Measures

```dax
Total Sales = SUM(Orders[Sales])

Total Profit = SUM(Orders[Profit])

Total Quantity = SUM(Orders[Quantity])

Avg Sales = AVERAGE(Orders[Sales])

YoY Sales Growth =
  DIVIDE(
    [Total Sales] - CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date])),
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
  )
```

---

## 🎨 Design Theme

| Element | Details |
|---|---|
| Background | Dark green gradient |
| Primary Accent | Cyan / Blue |
| Secondary Accent | Gold / Yellow |
| Tertiary Accent | Orange / Red |
| Font | Segoe UI (Power BI default) |
| Report Pages | 2 pages with consistent dark theme |

---

## 📈 Key Business Insights

- **Consumer segment** dominates at 48% of total sales
- **Office Supplies** is the best-performing category at 0.64M
- **Standard Class** shipping accounts for the majority of shipments (0.33M)
- **California** leads all states with 0.34M — nearly double New York (0.19M)
- **Payment modes are evenly split** (~33% each: Online, Cards, COD)
- **December** shows a consistent profit spike in both 2019 and 2020
- **2020 sales** trended higher than 2019, especially in Q4

---

## 👤 Author

**Rajeswari**
🔗 GitHub: [@29Rajeswari](https://github.com/29Rajeswari)

---

> **Note:** This dashboard uses a sample Superstore-style retail dataset commonly used for Power BI practice and data visualization learning.
