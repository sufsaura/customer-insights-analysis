# Customer Insights Analysis
### Customer Segmentation, Revenue Analysis & Churn-Risk Identification

## Project Overview

This project explores customer purchasing behaviour using SQL and Microsoft Excel.

The objective is to understand how customers contribute to revenue, identify valuable customer segments, examine purchasing inactivity, and present actionable insights through an Excel dashboard.

The project follows an end-to-end analytical workflow, from querying customer transaction data and calculating RFM metrics to segmenting customers and communicating the results through business-focused visualizations.

**Project Type:** Personal Data Analytics Project  
**Tools:** SQL, SQLite, Microsoft Excel  
**Dataset:** Synthetic Indian retail dataset  
**Focus Areas:** Customer Analytics, RFM Segmentation, Revenue Analysis, Churn-Risk Analysis

---

## Business Problem

Businesses need to understand which customers generate the most revenue, which customers purchase frequently, and which customers may require re-engagement.

Without structured customer analysis, it can be difficult to prioritize retention efforts, identify valuable customer groups, and understand purchasing patterns.

This project addresses the following business questions:

1. How many customers and orders are represented in the dataset?
2. Which customer segments contribute the most revenue?
3. Which customers have the highest historical spending?
4. How are customers distributed across RFM-based segments?
5. How many customers have been inactive for 90 days or longer?
6. How can customer and revenue insights be communicated through an interactive-looking, easy-to-understand dashboard?

---

## Dataset

The project uses a synthetic Indian retail dataset organized into three main tables:

| Table | Description |
|---|---|
| Customers | Customer identifiers and customer information |
| Products | Product identifiers and product information |
| Orders | Customer transactions, order dates, quantities, and unit prices |

The dataset is intended for analytical practice and portfolio demonstration. It does not represent verified results from a real company.

---

## Tools and Technologies

### SQL / SQLite
- Querying and aggregating customer transaction data
- Joining related tables
- Calculating customer-level purchasing metrics
- Creating reusable SQL views
- Implementing RFM-based customer segmentation
- Identifying customers with extended purchasing inactivity
- Ranking customers by historical spending

### Microsoft Excel
- Importing and organizing analytical results
- Creating KPI summaries
- Building customer segment summary tables
- Calculating revenue percentages
- Visualizing monthly revenue trends
- Comparing customer segments
- Presenting customer and churn-risk metrics in a dashboard

---

## Analytical Methodology

### 1. Data Exploration

Explored the Customers, Products, and Orders tables to understand the dataset structure and relationships.

### 2. Customer-Level Analysis

Calculated customer-level purchasing metrics, including:

- Recency: Days since the customer's last recorded purchase
- Frequency: Number of recorded purchases or orders, according to the dataset's calculation
- Monetary Value: Historical spending attributed to each customer

### 3. RFM Scoring

Assigned recency, frequency, and monetary scores to support customer comparison and segmentation.

Combined the three scores into an overall RFM score.

### 4. Customer Segmentation

Grouped customers into five segments:

| Segment | Analytical Purpose |
|---|---|
| High Value | Identify customers with high overall RFM scores |
| Loyal | Identify customers with strong frequency and recency scores |
| At Risk | Identify customers with 90–179 days of inactivity, unless assigned a higher-priority segment |
| Lost | Identify customers with 180 or more days of inactivity, unless assigned a higher-priority segment |
| Regular | Group remaining customers |

The segmentation rules prioritize High Value and Loyal customers before applying the At Risk and Lost labels. Therefore, segment membership and the overall 90-day inactivity population are separate classifications.

### 5. Churn-Risk Identification

Flagged customers whose most recent recorded purchase was at least 90 days ago.

This is an inactivity-based churn-risk indicator, not confirmation that every flagged customer has permanently churned.

### 6. Dashboard Development

Built an Excel dashboard to communicate customer, revenue, segment, and inactivity metrics.

The dashboard includes KPI summaries, customer segment comparisons, monthly revenue trends, top-spending customers, and churn-risk indicators.

---

## Key Results

The analysis produced the following results:

| Metric | Result |
|---|---:|
| Total Customers | 999 |
| Total Orders | 8,000 |
| Total Historical Revenue | ₹47,175,026 |
| Average Order Value | Approximately ₹5,896.88 |
| Customers Inactive for 90+ Days | 901 |
| 90+ Day Inactivity Rate | 90.19% |

### Customer Segment Results

| Customer Segment | Customer Count | Historical Revenue |
|---|---:|---:|
| High Value | 176 | ₹16,909,608 |
| Loyal | 110 | ₹4,706,097 |
| At Risk | 220 | ₹7,191,609 |
| Lost | 468 | ₹16,661,255 |
| Regular | 25 | ₹1,706,457 |

*Note: Segment revenue figures are shown as reported in the analysis. Small differences in the displayed totals can occur due to rounding or transcription; the workbook's calculated values should be treated as the source of truth.*

---

## Business Insights

### 1. High Value Customers

The High Value segment contains 176 customers and contributes approximately ₹16.91 million in historical revenue.

**Potential action:** Explore ways to retain these customers through relevant loyalty benefits, personalized offers, and continued customer engagement.

### 2. Lost Customers

The Lost segment contains 468 customers and represents approximately ₹16.66 million in historical revenue.

**Potential action:** Investigate previous purchasing patterns and test targeted re-engagement campaigns to assess whether some of these customers can be recovered.

Historical revenue should not be interpreted as guaranteed recoverable revenue.

### 3. Customer Inactivity

A total of 901 customers, representing 90.19% of the customer base, meet the project's 90-day inactivity threshold.

**Potential action:** Investigate inactivity patterns and prioritize outreach using customer value, purchasing history, and the length of inactivity.

This result is based on a synthetic dataset and should not be interpreted as an observed churn rate for a real business.

### 4. Customer Value Concentration

The High Value and Lost segments both represent substantial historical revenue contributions.

**Potential action:** Evaluate retention opportunities for valuable customers while separately investigating reactivation opportunities for previously valuable inactive customers.

---

## Dashboard Features

The Excel dashboard presents:

- Total customer count
- Total historical revenue
- Total order count
- Average order value
- Customers inactive for 90+ days
- 90+ day inactivity rate
- Customer segment summary
- Revenue by customer segment
- Customer distribution by segment
- Monthly revenue trend
- Top 10 customers by historical spending
- Churn-risk summary

---

## Recommendations

Based on the analysis, the following actions could be investigated:

1. Develop retention strategies for high-value customers.
2. Evaluate re-engagement campaigns for previously valuable inactive customers.
3. Monitor customer inactivity using a consistent definition.
4. Track revenue and customer segment changes over time.
5. Investigate purchasing patterns to identify opportunities for improving repeat purchases.
6. Use customer value and inactivity together when prioritizing retention activities.

These are analytical recommendations for further investigation, not claims that the strategies have already produced business results.

---

## Project Structure

```text
customer-insights-analysis/
│
├── README.md
├── data/
│   ├── customers.csv
│   ├── products.csv
│   └── orders.csv
│
├── sql/
│   ├── customer_analysis.sql
│   └── customer_segmentation.sql
│
├── excel/
│   └── Customer_Insights_Analysis.xlsx
│
└── screenshots/
    └── customer_insights_dashboard.png
```

*The structure above is the recommended organization. Include only files and folders that you have actually created.*

---

## Skills Demonstrated

- SQL querying and data aggregation
- Relational data analysis
- SQLite views and reusable queries
- RFM customer segmentation
- Customer purchasing behaviour analysis
- Revenue analysis
- Inactivity-based churn-risk identification
- Microsoft Excel formulas
- Dashboard development and data visualization
- Business insight communication

---

## Limitations

- The dataset is synthetic and may not represent actual retail customer behaviour.
- The analysis reflects the records and date range available in the dataset.
- A 90-day inactivity threshold is a project-defined indicator and may not be suitable for every business.
- Inactivity does not independently establish permanent customer churn.
- The recommendations have not been validated through real-world business experiments.

---

## Conclusion

This project demonstrates how SQL and Excel can be used together to analyze customer purchasing behaviour, calculate RFM metrics, segment customers, evaluate historical revenue, and identify potential retention priorities.

The final dashboard translates the analysis into a business-oriented summary intended to support customer relationship and retention discussions.

---

**Created by Sufiyan**  
Aspiring Data Analyst | SQL | Excel | Power BI | Python
