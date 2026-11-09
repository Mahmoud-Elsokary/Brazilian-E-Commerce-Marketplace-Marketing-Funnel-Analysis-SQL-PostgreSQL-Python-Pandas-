# Brazilian E-Commerce Public Dataset by Olist — SQL Exploratory Data Analysis (EDA)

A comprehensive SQL-based exploratory data analysis examining Olist's marketing funnel, seller acquisition, seller performance, and marketplace operational efficiency.

## 📋 Table of Contents

1. [Business Problem](#business-problem)

2. [Dataset Overview](#dataset-overview)

3. [Key Analysis & Results](#key-analysis--results)

4. [Limitations & Next Steps](#limitations--next-steps)

## 1. Business Problem

Olist connects small-to-medium businesses across Brazil to various marketplaces through a single contract. Managing this ecosystem effectively requires understanding the full lifecycle—from **marketing lead acquisition and conversion**, to **seller activation and revenue generation**, down to **marketplace sales and delivery operations**.

This project addresses key business questions to optimize acquisition channels, improve seller onboarding and activation, enhance logistics performance, and identify customer retention challenges.

## 2.  About the Data

The analysis is built using PostgreSQL and Pandas by combining multiple relational tables from the Brazilian E-Commerce Public Dataset by Olist:

* **`marketing_qualified_leads`**: Tracks lead origins, first contact dates, and acquisition channels.

* **`closed_deals`**: Contains information on converted leads, seller IDs, business segments, and won dates.

* **`orders`**: Records order purchase timestamps, delivery statuses, estimated delivery dates, and customer IDs.

* **`order_items`**: Details item pricing, order quantities, and seller associations.

* **`customers`**: Captures customer location details (states) and unique customer identifiers.

## 3. Show the Results of Your Analysis

### Phase 1: Marketing Lead Acquisition & Conversion

* **Top Lead Sources:** Organic Search generates the highest volume of leads (**28.70%**), followed by Paid Search (**19.83%**) and Social (**16.88%**). Together, these three channels account for **65.41%** of total leads.

* **Conversion Efficiency:** Paid Search achieves the highest conversion rate among identifiable major channels at **12.30%**, closely followed by Organic Search (**11.80%**).

* **Sales Cycle:** Direct Traffic has the shortest average sales cycle (\~32 days, median 11 days), while Social Media has the longest (\~61 days).

### Phase 2: Seller Acquisition & Activation

* **Top Business Segments:** Home Decor leads in acquired sellers (**12.47%**), followed by Health & Beauty (**11.05%**) and Car Accessories (**9.14%**).

* **Activation Gap:** Only **45.13%** of acquired sellers (380 out of 842) became active on the marketplace by generating orders, and **44.66%** successfully fulfilled delivered customer orders—highlighting a major drop-off during onboarding.

### Phase 3: Seller Performance & Revenue

* **Top Revenue Drivers:** Watches generate the highest product revenue (**\$115,901.08**) despite having only 2 active sellers out of 8 acquired sellers, indicating extreme revenue concentration. Health & Beauty recorded the highest volume of delivered orders (**693 orders**).

* **Segment Value:** Small Appliances achieves a high average revenue per acquired seller (**\$3,972.91**).

### Phase 4: Marketplace Sales & Operations

* **Order Fulfillment:** **97.02%** of orders (96,478 out of 99,441) were successfully delivered.

* **Delivery Performance:** **91.89%** of delivered orders arrived earlier than estimated, while **6.77%** were delivered late. State-level analysis shows higher late-delivery rates in Alagoas (**21.41%**) and Maranhão (**17.43%**).

* **Customer Retention Challenge:** **97.00%** of customers made only a single purchase, with just **3.00%** making repeat purchases.

## 4. Limitations & Next Steps

### Limitations Faced

* **Data Attribution Gaps:** Unknown sources account for **14.49%** of leads, limiting precise channel performance evaluation.

* **Small Sample Sizes:** Certain business segments (e.g., display ads, specific states like Roraima) have very small sample sizes, requiring cautious interpretation of their conversion rates and delivery metrics.

### Recommendations & Next Steps

1. **Improve Attribution:** Enhance tracking mechanisms to minimize unassigned lead origins.

2. **Optimize Social Media Funnel:** Investigate why Social Media generates high lead volume but suffers from a low conversion rate (**5.56%**).

3. **Streamline Seller Onboarding:** Re-examine the seller activation pipeline to convert more than the current **45.13%** active seller rate.

4. **Logistics Optimization:** Focus on improving delivery efficiency in underperforming states such as Alagoas and Maranhão.

5. **Customer Retention Strategies:** Develop loyalty and engagement programs to address the low repeat-purchase rate (**3.00%**).