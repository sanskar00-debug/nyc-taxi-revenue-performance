
# 🚖 NYC Taxi Performance & Revenue Visual Analytics

An end-to-end business intelligence and data visualization project analyzing New York City taxi ride patterns, revenue dynamics, consumer payment preferences, and hourly demand distributions across boroughs using **Tableau** and **Qlik Sense**.

---

## 📌 Project Overview

* **Dataset Size:** 6,404 cleaned trip records
* **Total Gross Revenue Analyzed:** $118,190.63
* **Primary Tools:** Tableau Desktop / Tableau Public, Qlik Sense, CSV
* **Core Metrics Tracked:** Total Fare Revenue, Average Distance per Trip, Hourly Demand Density, Payment Share, and Geographic Concentration

---

## 📁 Repository Structure

```text
nyc-taxi-tableau-qlik-analytics/
├── data/
│   ├── taxis_cleaned.csv            # Cleaned NYC TLC ride-level dataset
├── assets/
│   ├── tableau_dashboard.png        # High-resolution screenshot of the Tableau dashboard
├── tableau/
│   └── nyc_taxi_analysis.twbx       # Packaged Tableau Workbook
└── README.md                        # Complete project documentation.
```

## 📊 Business Insights & Key Findings
 * Manhattan Drives the Bulk of Revenue:
   * Manhattan generates $87,899.80 (74.4% of total platform revenue).
   * Queens ranks second with $20,771.89 (17.6%), heavily driven by long-haul airport transit to and from JFK and LaGuardia.
   * Brooklyn ($7,265.18 / 6.1%) and the Bronx ($2,253.76 / 1.9%) account for minimal yellow taxi market share.
 * Cashless Payments Dominate:
   * Credit Card: 71.8% of trips (4,598 rides).
   * Cash: 28.2% of trips (1,806 rides).
   * Digital payments represent the majority of recorded transactions and consistently yield higher reported tip amounts compared to cash.
 * Trip Distance and Pricing Outliers:
   * The average trip distance is 3.03 miles, with a mean base fare of $13.03 and average tip of $1.97.
   * While trip fare generally scales linearly with distance, distinct horizontal clusters appear at standard flat-rate thresholds (e.g., $52 JFK flat rate before surcharges).
 * Demand Bottlenecks and Peak Windows:
   * Demand peaks sharply between 17:00 and 20:00 (5:00 PM – 8:00 PM) on weekdays, aligning with corporate transit hours.
   * Friday and Saturday evenings sustain elevated demand past midnight, signaling weekend entertainment travel.
   
## 🛠️ Dashboard Architecture
1. Tableau Implementation
 * Hourly Demand Heatmap: Maps trip counts across a discrete 7 x 24 grid (Weekday vs. Hour of Day) with diverging color gradients to highlight peak congestion windows.
 * Distance vs. Fare Scatter Plot: Plotted at the individual trip level (disaggregated) with opacity and borders applied to show density, outliers, and flat-rate fares categorized by payment type.
 * Borough Revenue Ranking: Horizontal sorted bar chart illustrating total revenue generation across boroughs, paired with direct bar labels to reduce visual clutter.
 * Payment Method Distribution: Bar comparison visualizing the volume split between cash and card transactions.
 * Interactive Dashboard Actions: Configured cross-filtering actions so clicking any borough or time block dynamically filters all companion views.
