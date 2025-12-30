# Retail Customer & Revenue Analysis

## Project Overview
This project analyzes transaction-level retail data to understand customer purchasing behavior and identify high-impact customer segments. Rather than predicting revenue mechanically, the analysis focuses on **behavioral patterns** that inform marketing, retention, and revenue optimization strategies.

Using **Recency, Frequency, and Monetary (RFM)** metrics, customers are segmented into distinct groups to support data-driven decision-making in a retail context.

## Business Objective
**How can retail customers be segmented based on purchasing behavior to improve targeting, retention, and revenue strategy?**

Retail businesses often face diminishing returns from one-size-fits-all marketing. This project demonstrates how transaction data can be transformed into actionable customer segments.

## Dataset
- **Source:** Retail transaction dataset (100,000 rows)
- **Granularity:** Transaction-level
- **Key fields:**
  - CustomerID
  - ProductCategory
  - Quantity
  - Price
  - DiscountApplied (%)
  - TransactionDate
  - PaymentMethod
  - TotalAmount

## Exploratory Data Analysis
Key EDA steps included:
- Distribution analysis of quantity, unit price, and total transaction value
- Payment method usage comparison
- Product category transaction patterns
- Identification of right-skewed revenue distribution and repeat purchase behavior

**Key observations:**
- Transaction values are right-skewed, with a small subset of high-value purchases
- Most transactions involve small basket sizes
- Payment methods are evenly distributed across customers
- Product categories differ meaningfully in average transaction value

## Feature Engineering
Customer-level features were engineered using **RFM methodology**:

- **Recency:** Days since last purchase
- **Frequency:** Number of transactions
- **Monetary:** Total spend across all transactions

These features capture customer engagement intensity and value over time.

## Modeling Approach
An **unsupervised learning approach** was used to segment customers:

- Features scaled using StandardScaler
- **KMeans clustering** applied with 4 clusters
- Clusters interpreted using average RFM metrics

This approach avoids target leakage and focuses on behavioral structure rather than deterministic prediction.

## Customer Segmentation Results
Four distinct customer segments were identified:

- **High-Value Loyal Customers:** Recent, frequent purchasers with high total spend  
  → Best targets for loyalty and retention programs

- **High-Spend, Low-Frequency Customers:** Infrequent but high-value buyers  
  → Opportunity for reactivation and personalized outreach

- **Low-Value Customers:** Infrequent, low-spend customers  
  → Minimal marketing investment recommended

- **Recent Moderate Customers:** New or returning customers with moderate spend  
  → Upsell and cross-sell opportunities

## Business Takeaways
- A small subset of customers drives a disproportionate share of total revenue
- Customer value varies significantly across recency and frequency dimensions
- RFM segmentation provides a scalable framework for targeted retail strategies

## Limitations
- No inventory or stock-on-hand data available
- Promotional causality cannot be inferred
- Results reflect historical behavior, not future guarantees

## Next Steps
- Track customer movement between segments over time
- Incorporate promotion response and pricing sensitivity
- Extend segmentation with product-level or margin data

## Tools Used
- Python
- Pandas
- NumPy
- Matplotlib & Seaborn
- Scikit-learn

## Key Takeaway
Retail transaction data can be transformed into actionable customer insights using RFM segmentation, enabling smarter marketing, retention, and revenue decisions without relying on fragile predictive assumptions.
