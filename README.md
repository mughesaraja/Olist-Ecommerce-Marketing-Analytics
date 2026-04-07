# Olist-Ecommerce-Marketing-Analytics
End-to-end analysis of 100k+ Brazilian e-commerce orders. Features SQL data modeling, RFM customer segmentation in Python, and a Power BI executive dashboard.

## Executive Dashboard
![Executive Overview](https://github.com/mughesaraja/Olist-Ecommerce-Marketing-Analytics/blob/main/Images/Executive%20Overview.png)
*Figure 1: High-level overview of Revenue (16.19M) and Order Volume (115.72K) from 2016-2018.*

My analysis reveals a critical 'Customer Satisfaction Cliff' where average review scores plummet from 4.5 to 2.0 stars as soon as a delivery exceeds its estimated arrival date by even 24 hours. Despite 80% of orders arriving early, the 'Long Tail' of late deliveries (some exceeding 50 days) acts as the primary driver for 1-star reviews across all Brazilian states. These findings suggest that for Olist to scale, the focus must shift from 'average speed' to 'consistency,' as even minor delays disproportionately damage brand reputation.

**Key Business Insights & Findings**
**1. Logistics & Delivery Performance**
The "Satisfaction Cliff": 
My analysis reveals a critical 'Customer Satisfaction Cliff' where average review scores plummet from 4.5 to 2.0 stars as soon as a delivery exceeds its estimated arrival date.

![Delivery Delay vs Review Score](Images/customer_insights.png)
*Figure 2: Correlation analysis showing the sharp decline in customer sentiment at the 0-day delay threshold.*

Analysis confirms a direct correlation between delivery speed and customer sentiment. While early deliveries maintain a 4.5+ star average, review scores plummet to 2.0 stars the moment an order is even 24 hours late.
Conservative Estimates: Olist successfully manages expectations by over-estimating delivery times; 80% of orders arrive before the "Estimated Delivery Date," which acts as a major driver for 5-star reviews.
The Long Tail Risk: While the average delay is low, "Outlier" deliveries (orders 20+ days late) are the primary cause of brand detractors, regardless of the product quality.

**2. Revenue & Sales Trends**
Health & Beauty and Watches & Gifts emerge as the highest revenue-generating categories.
![Product Category and Delay Distribution](Images/sales_and_operational_analysis.png)
*Figure 3: Revenue by category (left) and the distribution of delivery delays (right), highlighting the 'Long Tail' risk.*
Consistent Growth: The platform showed a steady upward trajectory in revenue from 2016 through 2018, indicating successful market penetration in the Brazilian e-commerce space.
Category Dominance: Health & Beauty and Watches & Gifts are the highest revenue-generating categories, suggesting a customer base that prioritizes personal care and high-value discretionary items.

**3. Regional Variations (Slicer Insights)**
Infrastructure Gaps: Using the State Slicer, it is evident that states in the North and Northeast (e.g., AM, RR) experience wider delivery distributions and lower average review scores compared to the Southeast (SP, RJ), highlighting a need for localized logistics partnerships in remote regions.

**Data & Methodology**
Due to GitHub's file size limits, the raw data is not hosted here. 
The dataset used in this analysis is the **Brazilian E-Commerce Public Dataset by Olist**. 

* **Primary Data Source:** Download the Data: Kaggle - Olist Dataset [Download CSVs from Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
* The dataset used in this project is the Brazilian E-Commerce Public Dataset by Olist. Due to the file size (100MB+), the raw data is not hosted in this repository.

**Key Findings**
The Satisfaction Cliff: Customer sentiment stays high (4.5 stars) for early deliveries but drops instantly to 2.0 stars the moment a delivery is 1 day late.

Conservative Estimates: 80% of orders arrive before the estimated date, suggesting Olist successfully manages expectations through "under-promising and over-delivering."

Regional Disparity: States in the North/Northeast show significantly wider delivery tails compared to the Southeast, impacting local brand reputation.
