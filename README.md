# Amazon Marketplace Sales Performance Analysis

## Overview
End-to-end exploratory data analysis of 100,000 Amazon marketplace orders spanning 2020–2024 across 5 countries and 6 product categories. The project follows a structured analytical workflow — from problem definition and data quality investigation through to EDA, insight generation, and business recommendations.

**Tools:** Python (Pandas, Seaborn, Matplotlib) | Power BI | Jupyter Notebook  
**Dataset:** 100,000 rows × 20 columns  
**Period:** January 2020 – December 2024  

---

## Business Questions
1. Which product categories drive the most revenue?
2. What is the return rate across categories — and where is it highest?
3. How do discounts affect average order value?
4. Which payment methods are most preferred?
5. How has revenue trended year over year from 2020–2024?
6. Which markets (countries) contribute the most to sales?

---

## Dataset Columns

| Column | Description |
|---|---|
| OrderID | Unique order identifier |
| OrderDate | Date the order was placed |
| CustomerID | Unique customer identifier |
| CustomerName | Customer full name |
| ProductID | Unique product identifier |
| ProductName | Name of the product |
| Category | Product category |
| Brand | Brand name |
| Quantity | Number of units ordered |
| UnitPrice | Price per unit (USD) |
| Discount | Discount applied (0–0.30) |
| Tax | Tax amount (USD) |
| ShippingCost | Shipping cost (USD) |
| TotalAmount | Final order value (USD) |
| PaymentMethod | Payment method used |
| OrderStatus | Order status (Delivered/Shipped/Pending/Returned/Cancelled) |
| City | Customer city |
| State | Customer state |
| Country | Customer country |
| SellerID | Unique seller identifier |

---

## Project Structure

```
amazon-marketplace-analysis/
├── Amazon_Marketplace_Analysis.ipynb   # Main analysis notebook
├── Amazon.csv                          # Dataset
├── chart1_revenue_by_category.png      # Revenue by category bar chart
├── chart2_return_rate_by_category.png  # Return rate by category
├── chart3_yearly_revenue_trend.png     # YoY revenue trend line chart
├── chart4_discount_impact.png          # Discount vs avg order value
├── chart5_payment_methods.png          # Payment method pie chart
├── chart6_revenue_by_country.png       # Revenue by country
└── README.md                           # This file
```

---

## Analysis Workflow

### Step 1 — Problem Definition
Defined 6 business questions to guide the analysis before touching any data.

### Step 2 — Data Loading & Initial Inspection
- Loaded dataset using Pandas
- Inspected shape, column types, and statistical summary
- Confirmed 100,000 rows × 20 columns

### Step 3 — Data Quality Investigation & Cleaning
Performed systematic checks across completeness, accuracy, and consistency dimensions:

| Check | Finding | Action |
|---|---|---|
| Null values | 0 nulls found | No action needed |
| Duplicate Order IDs | 0 duplicates | No action needed |
| Zero/Negative TotalAmount | 0 records | No action needed |
| Category label consistency | Verified consistent | Stripped & title-cased |
| Date format | String format | Converted to datetime, extracted Year/Month |

✅ Dataset passed all quality checks.

### Step 4 — Exploratory Data Analysis (EDA)
6 visualisations produced using Seaborn and Matplotlib:
- Revenue by category (bar chart)
- Return rate by category (bar chart with avg line)
- Year-over-year revenue trend 2020–2024 (line chart)
- Discount impact on average order value (bar chart)
- Payment method distribution (pie chart)
- Revenue by country (bar chart)

### Step 5 — Business Insights & Recommendations
6 key findings with actionable recommendations.

---

## Key Findings

**1. Revenue is Balanced Across All 6 Categories**  
Electronics leads at ~$15.58M but all categories are within 3% of each other — a well-diversified portfolio with no single-category dependency.

**2. Home & Kitchen Has the Highest Return Rate (3.21%)**  
Electronics has the lowest return rate at 2.82%. Home & Kitchen and Books are above average — signalling potential product-fit or quality issues worth investigating.

**3. Heavy Discounts Significantly Erode Order Value**  
Average order value drops from ~$988 at 0% discount to ~$727 at 30% discount — a 26% reduction. The business should evaluate whether volume gains at higher discounts offset this margin loss.

**4. Revenue Has Been Flat 2020–2024 (~$18.3M/year)**  
Year-over-year revenue is remarkably consistent with no meaningful growth. This could indicate market saturation or absence of a growth strategy.

**5. Credit Cards Dominate (35%) — UPI at 15% is Growing**  
UPI adoption signals strong digital payment penetration, particularly in the Indian market.

**6. United States Drives 70% of Total Revenue**  
India and Canada are secondary markets with existing order volumes but untapped growth potential.

---

## Recommendations
- Investigate return drivers in Home & Kitchen — product descriptions, sizing, or quality issues
- Cap maximum discount at 20% to protect average order value
- Develop targeted growth strategies for India and Canada markets
- Introduce seasonal promotions to break the flat YoY revenue trend
- Expand UPI and digital payment options for the Indian market segment

---

## How to Run

```bash
# Clone the repository
git clone https://github.com/soumyathamke/amazon-marketplace-analysis.git
cd amazon-marketplace-analysis

# Install dependencies
pip install pandas seaborn matplotlib jupyter

# Launch notebook
jupyter notebook Amazon_Marketplace_Analysis.ipynb
```

---

## Author
**Soumya Thamke**  
[LinkedIn](https://linkedin.com/in/soumya-thamke-b04082250) | [GitHub](https://github.com/soumyathamke) | [Portfolio](https://soumyathamke.github.io/soumya-portfolio/)
