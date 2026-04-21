# Olist-Ecommerce-Marketing-Analytics
End-to-end analysis of 100k+ Brazilian e-commerce orders. Features SQL data modeling, RFM customer segmentation in Python, and a Power BI executive dashboard.

## Executive Dashboard
![Executive Overview](https://github.com/mughesaraja/Olist-Ecommerce-Marketing-Analytics/blob/main/Images/Executive%20Overview.png)

*Figure 1: High-level overview of Revenue (16.19M) and Order Volume (115.72K) from 2016-2018.*

My analysis reveals a critical 'Customer Satisfaction Cliff' where average review scores plummet from 4.5 to 2.0 stars as soon as a delivery exceeds its estimated arrival date by even 24 hours. Despite 80% of orders arriving early, the 'Long Tail' of late deliveries (some exceeding 50 days) acts as the primary driver for 1-star reviews across all Brazilian states. These findings suggest that for Olist to scale, the focus must shift from 'average speed' to 'consistency,' as even minor delays disproportionately damage brand reputation.

---

## Customer Segmentation Framework (RFM Analysis)
To move beyond aggregate totals, I developed an RFM (Recency, Frequency, Monetary) model in Python to segment the 100k+ customer base. This allows the business to tailor marketing strategies based on actual purchasing behavior:

**Champions:** Recent, frequent, and high-spending customers.

**At-Risk:** High-value customers who haven't purchased in a long time (critical for churn prevention).

**Hibernating:** Low-frequency, low-spend customers who may not be worth high marketing acquisition costs.

**Technical Implementation:** I used Pandas to calculate individual scores for each customer, then assigned them to segments using Quantiles. These segments were then exported to the Power BI dashboard to allow for dynamic filtering by "Customer Health."

---
## Dynamic Opportunity Modeling in Power BI"

**DAX-Driven Gap Analysis:** Developed custom DAX measures to calculate the variance between the Python-generated 'Predicted Revenue' and 'Actual Revenue' in real-time.

**Interactive 'Hit List' Generation:** Utilised Conditional Formatting and Top-N Filters to create an automated "Priority Table." This allows stakeholders to toggle by industry or plan_tier to instantly identify the highest-value expansion opportunities.

**Seamless Tool Integration:** Established a workflow where the Machine Learning outputs (from Colab) are ingested into a Power BI Star Schema, bridging the gap between advanced data science and front-end business intelligence.

**Root Cause Analysis (The 'Satisfaction Cliff'):** Using Power BI, I identified a critical correlation where delivery delays exceeding 24 hours led to a 55% drop in average review scores. This insight allowed me to provide a strategic recommendation on shipping buffers.

---

## Strategic Recommendations**

**1. Logistics & Delivery Performance**
**The "Satisfaction Cliff":** 
My analysis reveals a critical 'Customer Satisfaction Cliff' where average review scores plummet from 4.5 to 2.0 stars as soon as a delivery exceeds its estimated arrival date.
Customer sentiment stays high (4.5 stars) for early deliveries but drops instantly to 2.0 stars the moment a delivery is even 24 hours late. This suggests that for Olist, "on-time" is the baseline for survival, not a bonus.

![Delivery Delay vs Review Score](https://github.com/mughesaraja/Olist-Ecommerce-Marketing-Analytics/blob/main/Images/Customer%20Insights.png)
*Figure 2: Correlation analysis showing the sharp decline in customer sentiment at the 0-day delay threshold.*

Analysis confirms a direct correlation between delivery speed and customer sentiment. While early deliveries maintain a 4.5+ star average, review scores plummet to 2.0 stars the moment an order is even 24 hours late.
**Conservative Estimates:** Olist successfully manages expectations by over-estimating delivery times; 80% of orders arrive before the "Estimated Delivery Date," which acts as a major driver for 5-star reviews.
80% of orders arrive before the estimated date. This indicates that Olist successfully manages expectations through an "under-promise and over-deliver" logic, which maintains the 4.5-star average for the majority of the fleet.
**The Long Tail Risk:** While the average delay is low, "Outlier" deliveries (orders 20+ days late) are the primary cause of brand detractors, regardless of the product quality.
**The Long-Tail Paradox (Outliers):** While review scores plummet after day 1, there is a slight "upward tick" in scores for extremely late orders (60+ days).
 - Insight: This is likely Survivor Bias—customers who don't cancel after two months are often those who highly value the specific product.
 - Recommendation: Management should ignore this slight uptick; the "Long Tail" of deliveries (20+ days late) remains the primary driver of 1-star reviews across all Brazilian states.

**2. Revenue & Sales Trends**
Health & Beauty and Watches & Gifts emerge as the highest revenue-generating categories.
![Product Category and Delay Distribution](https://github.com/mughesaraja/Olist-Ecommerce-Marketing-Analytics/blob/main/Images/Sales%20%26%20Operational%20Analysis.png)
*Figure 3: Revenue by category (left) and the distribution of delivery delays (right), highlighting the 'Long Tail' risk.*
Consistent Growth: The platform showed a steady upward trajectory in revenue from 2016 through 2018, indicating successful market penetration in the Brazilian e-commerce space.
Category Dominance: Health & Beauty and Watches & Gifts are the highest revenue-generating categories, suggesting a customer base that prioritizes personal care and high-value discretionary items.

**3. Regional Variations (Slicer Insights)**
Infrastructure Gaps: Using the State Slicer, it is evident that states in the North and Northeast (e.g., AM, RR) experience wider delivery distributions and lower average review scores compared to the Southeast (SP, RJ), highlighting a need for localized logistics partnerships in remote regions.
**Regional Disparity:** Infrastructure gaps in the North/Northeast result in significantly wider delivery distributions compared to the Southeast, directly impacting local brand reputation and repeat purchase rates.

--- 

## Data Architecture & SQL Modelling
**Star Schema Design:** Structured the underlying data using SQL-style joins to unify 5 disparate tables (Orders, Payments, Products, Customers, and Geolocation).
**Query Optimisation:** Ensured the model remains performant for Power BI by pre-aggregating key metrics, demonstrating a "Large Dataset" mindset.


**Data & Methodology**
Due to GitHub's file size limits, the raw data is not hosted here. 
The dataset used in this analysis is the **Brazilian E-Commerce Public Dataset by Olist**. 

* **Primary Data Source:** Download the Data: Kaggle - Olist Dataset [Download CSVs from Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
* The dataset used in this project is the Brazilian E-Commerce Public Dataset by Olist. Due to the file size (100MB+), the raw data is not hosted in this repository.
