# Customer Marketing & Campaign Performance Dashboard

## Project Overview

This Power BI project analyzes customer demographics, purchasing behavior, product spending, purchase channels, and marketing campaign performance. The dashboard is designed to help understand customer behavior and evaluate which campaigns and product categories perform best.

## Power BI Project File

The complete interactive Power BI report is included in this repository:

**[Open / Download the Power BI .pbix file](Customer%20Marketing%20%26%20Campaign%20Performance%20Dashboard.pbix)**

## Dashboard Preview

![Customer Marketing & Campaign Performance Dashboard](dashboard/customer_marketing_campaign_dashboard.png)

## Key KPIs

- **Total Customers:** 2,240
- **Average Income:** 52.25K
- **Total Spend:** 1.36M
- **Response Rate:** 14.91%
- **Average Recency:** 49.11 days
- **Total Purchases:** 28,083

## Dashboard Analysis

### Spend by Product Category

- Wine generated the highest customer spend at approximately **680.8K**.
- Meat products were the second-largest category at approximately **374.0K**.
- Gold products contributed approximately **98.6K**.
- Fish, sweets, and fruit represented smaller portions of total spending.

### Customers by Country

- Spain represents the largest customer group with **1,095 customers**.
- Saudi Arabia has **337 customers** and Canada has **268 customers**.
- The dashboard also includes customers from Australia, India, Germany, USA, and Mexico.

### Purchases by Channel

- **Store Purchases:** 12,970
- **Web Purchases:** 9,150
- **Catalog Purchases:** 5,963

Store purchases are the largest purchase channel in the dataset.

### Customers by Education

- Graduation: **1,127 customers**
- PhD: **486 customers**
- Master: **370 customers**
- 2n Cycle: **203 customers**
- Basic: **54 customers**

### Campaign Performance

- Latest Campaign / Response: **14.91%**
- Campaign 4: **7.46%**
- Campaign 3: **7.28%**
- Campaign 5: **7.28%**
- Campaign 1: **6.43%**
- Campaign 2: **1.34%**

The latest campaign achieved the highest response rate among the campaign measures shown in the dashboard.

## Interactive Filters

The Power BI dashboard includes slicers for:

- Country
- Education

These filters allow users to explore how KPIs and customer behavior change across different segments.

## Tools & Skills Demonstrated

- Microsoft Power BI
- DAX Measures
- KPI Development
- Data Visualization
- Customer Segmentation
- Marketing Campaign Analysis
- Business Reporting
- Dashboard Design

## DAX Measures Used

Examples of measures used in the dashboard include:

```DAX
Total Customers =
DISTINCTCOUNT(marketing_data[ID])
```

```DAX
Total Spend =
SUM(marketing_data[MntWines]) +
SUM(marketing_data[MntFruits]) +
SUM(marketing_data[MntMeatProducts]) +
SUM(marketing_data[MntFishProducts]) +
SUM(marketing_data[MntSweetProducts]) +
SUM(marketing_data[MntGoldProds])
```

```DAX
Response Rate =
DIVIDE(
    SUM(marketing_data[Response]),
    COUNTROWS(marketing_data),
    0
)
```

```DAX
Total Purchases =
SUM(marketing_data[NumWebPurchases]) +
SUM(marketing_data[NumCatalogPurchases]) +
SUM(marketing_data[NumStorePurchases])
```

## Repository Structure

```text
Customer-Marketing-Campaign-Power-BI/
├── Customer Marketing & Campaign Performance Dashboard.pbix
├── README.md
├── data/
│   ├── marketing_data.csv
│   └── marketing_data_dictionary.csv
└── dashboard/
    └── customer_marketing_campaign_dashboard.png
```

## Author

**Syed Ali Qasim Rizvi**  
Data Analyst | Power BI | SQL | Excel | Tableau

Email: syedrizvi616@gmail.com
