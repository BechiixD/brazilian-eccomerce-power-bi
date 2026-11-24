# Project Brief

## Client and problem
A mid-size online marketplace. Management says: *"Sales are growing, but we don't know where we're losing money and customers. We need a dashboard to make decisions."*

## Business questions
1. How are revenue, orders and average order value (AOV) trending? Is there seasonality?
2. Which product categories and states drive the most revenue, and which underperform?
3. How does delivery performance (late vs on-time) affect review scores?
4. What share of customers buy again, and what does it mean for the business?
5. Which sellers concentrate the most sales, and is there a dependency risk?

## Data
[Olist Brazilian E-commerce dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle): ~100K orders from 2016 to 2018 across 9 relational tables.

## Assumptions
- **Revenue** = item `price`, excluding freight.
- Only orders with `order_status = "delivered"` count toward revenue, orders, AOV, reviews and late %.
- A customer is identified by `customer_unique_id`, because Olist creates a new `customer_id` for every order.
- The analysis window is **Jan 2017 – Aug 2018**. Data from 2016 and Sep–Oct 2018 is partial.
- Year-over-year comparisons use equal periods (Jan–Aug 2018 vs Jan–Aug 2017).

## Out of scope
- Freight and payment profitability (no cost data).
- Text analysis of review comments.
- Geolocation-level mapping (the geolocation table was dropped).
- Forecasting.

## Deliverables
1. This brief
2. [Data model documentation](data-model.md)
3. Power BI report (4 pages): Executive summary · Sales and products · Delivery and satisfaction · Customers and sellers
4. [Findings and recommendations](findings.md)
5. GitHub repo with README and screenshots

## Phases
Scoping → Clean and transform (Power Query) → Model (star schema) → DAX → Visuals → Docs and publish
