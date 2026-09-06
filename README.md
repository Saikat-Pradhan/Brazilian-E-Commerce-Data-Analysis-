# 🛒 Olist E-Commerce Analytics

### Customer Experience & Marketplace Performance Analysis

An end-to-end **Exploratory Data Analysis (EDA)** project using the Brazilian Olist e-commerce marketplace dataset. The project investigates **marketplace performance, customer satisfaction, delivery reliability, seller and geographic patterns, product categories, and payment behavior**.

By combining multiple transactional datasets, the analysis identifies the factors most strongly associated with customer satisfaction and dissatisfaction and translates the findings into **actionable business recommendations**.

---

## 📌 Table of Contents

* [📊 Project Overview](#-project-overview)
* [🎯 Business Problem](#-business-problem)
* [🎯 Objectives](#-objectives)
* [🗂️ Dataset](#️-dataset)
* [🛠️ Tools & Technologies](#️-tools--technologies)
* [📈 Key Performance Indicators](#-key-performance-indicators)
* [🔎 Analysis Performed](#-analysis-performed)
* [🔍 Root Cause Analysis](#-root-cause-analysis-of-low-review-scores)
* [💡 Key Findings](#-key-findings)
* [📋 Business Recommendations](#-business-recommendations)
* [🏁 Conclusion](#-conclusion)
* [📌 Project Highlights](#-project-highlights)
* [👤 Author](#-author)

---

## 📊 Project Overview

This project analyzes approximately **100,000 orders** from the Olist Brazilian e-commerce marketplace, covering the period from **September 2016 to October 2018**.

The analysis focuses on:

* 📈 Marketplace performance over time
* 🚚 Delivery performance and reliability
* ⭐ Customer satisfaction and review scores
* 🏪 Seller performance and geographic distribution
* 📦 Product category performance
* 💳 Payment methods and installment behavior
* 🔍 Factors associated with low customer review scores

### 🎯 Main Objective

The primary objective is to understand **what drives customer experience and marketplace performance** and identify the operational areas where improvements could have the greatest business impact.

---

## 🎯 Business Problem

Olist operates a large marketplace that connects customers and sellers across Brazil.

The central business question addressed in this project is:

> **What factors are most strongly associated with customer satisfaction, and which operational areas should Olist prioritize to improve marketplace performance?**

The analysis investigates relationships among:

* Orders
* Delivery performance
* Customer reviews
* Freight costs
* Sellers
* Customer geography
* Product categories
* Payment methods
* Order value

---

## 🎯 Objectives

The project addresses six core business questions.

### 1. 📈 Marketplace Performance

* How does order volume change over time?
* How does recorded revenue change over time?
* How do customer review scores change over time?
* Do commercial performance and customer experience move together?

### 2. 🚚 Delivery & Customer Satisfaction

* How does delivery time affect customer reviews?
* How does delivery delay relate to review scores?
* Do early, on-time, and late deliveries have different satisfaction levels?

### 3. 🏪 Seller & Geographic Analysis

* Which states generate the most seller activity?
* Which states have the highest customer order volume?
* Is freight cost associated with customer satisfaction?

### 4. 📦 Product Category Analysis

* Which categories generate the most orders?
* Which categories generate the most revenue?
* Which categories have unusually low customer satisfaction?

### 5. 💳 Payment Behavior

* Which payment methods are most frequently used?
* Which payment methods generate higher order values?
* Does payment behavior have a meaningful relationship with customer satisfaction?

### 6. 🔍 Root Cause Analysis

* What factors are most strongly associated with low review scores?
* How different are low-review orders from higher-review orders?
* Which operational metrics should management prioritize?

---

## 🗂️ Dataset

The project uses the **Olist Brazilian E-Commerce dataset** and combines **nine related datasets**:

| Dataset                                 | Description                                       |
| --------------------------------------- | ------------------------------------------------- |
| `olist_orders_dataset.csv`              | Order status and order lifecycle dates            |
| `olist_order_items_dataset.csv`         | Products, sellers, prices, and freight            |
| `olist_order_payments_dataset.csv`      | Payment methods, installments, and payment values |
| `olist_order_reviews_dataset.csv`       | Customer review scores and review information     |
| `olist_customers_dataset.csv`           | Customer identifiers and locations                |
| `olist_products_dataset.csv`            | Product-level information                         |
| `olist_sellers_dataset.csv`             | Seller identifiers and locations                  |
| `olist_geolocation_dataset.csv`         | Brazilian geolocation information                 |
| `product_category_name_translation.csv` | Portuguese-to-English category translation        |

### Dataset Size

| Dataset              |   Records | Columns |
| -------------------- | --------: | ------: |
| Orders               |    99,441 |       8 |
| Order Items          |   112,650 |       7 |
| Order Payments       |   103,886 |       5 |
| Order Reviews        |    99,224 |       7 |
| Customers            |    99,441 |       5 |
| Products             |    32,951 |       9 |
| Sellers              |     3,095 |       4 |
| Geolocation          | 1,000,163 |       5 |
| Category Translation |        71 |       2 |

### 📥 Dataset Source

[**Olist Brazilian E-Commerce Dataset — Kaggle**](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

---

## 🛠️ Tools & Technologies

### Programming Language

* **Python**

### Data Analysis

* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical operations

### Data Visualization

* **Matplotlib**
* **Seaborn**

### Development Environment

* **Google Colab**
* **Jupyter Notebook**

The analysis uses Pandas and NumPy for data processing and Matplotlib/Seaborn for visualization and exploratory analysis.

---

# 📈 Key Performance Indicators

The analysis produced the following headline KPIs:

| KPI                                     |               Value |
| --------------------------------------- | ------------------: |
| **Total Orders**                        |          **99,441** |
| **Total Recorded Payment Value**        | **R$16,008,872.12** |
| **Average Review Score**                |        **4.09 / 5** |
| **On-Time Delivery Rate**               |          **89.15%** |
| **Average Review — Early Deliveries**   |        **4.30 / 5** |
| **Average Review — On-Time Deliveries** |        **4.16 / 5** |
| **Average Review — Late Deliveries**    |        **2.57 / 5** |
| **Average Delivery Time**               |      **12.56 days** |
| **Median Delivery Time**                |      **10.22 days** |

> **Key takeaway:** Delivery performance emerges as one of the strongest themes in the analysis and has a substantial relationship with customer satisfaction.

---

# 🔎 Analysis Performed

## 1. 📈 Marketplace Performance Over Time

The project examines monthly:

* Order volume
* Recorded revenue
* Average review score

The analysis shows that **order volume and revenue generally increased from 2017 into 2018**, with particularly strong activity around late 2017 and early 2018.

The final September and October 2018 observations contain very small numbers of orders. Therefore, the sharp decline at the end of the time series **should not be interpreted as a definitive marketplace collapse**.

---

## 2. 🚚 Delivery Performance & Customer Satisfaction

Delivery performance is the **strongest operational theme** identified in the project.

The analysis compares customer review scores across delivery-performance groups:

| Delivery Status | Average Review Score |
| --------------- | -------------------: |
| Early           |             **4.30** |
| On Time         |             **4.16** |
| 1–3 Days Late   |             **3.77** |
| 4–7 Days Late   |             **2.32** |
| 8–14 Days Late  |             **1.75** |
| 15+ Days Late   |             **1.71** |

### 🔑 Key Insight

> **As delivery delays increase, average customer review scores decline substantially.**

This makes **delivery reliability a critical customer-experience KPI**.

---

## 3. 🏪 Seller & Geographic Patterns

Seller activity is geographically concentrated across Brazil.

### Leading Seller States

1. **São Paulo (SP)**
2. **Paraná (PR)**
3. **Minas Gerais (MG)**
4. **Rio de Janeiro (RJ)**
5. **Santa Catarina (SC)**

São Paulo also has the **highest customer order volume by a wide margin**.

### 🚚 Freight & Customer Satisfaction

The analysis reports a correlation of approximately:

**-0.089**

between freight value and review score.

This represents a **weak negative association**:

> Higher freight costs are associated with slightly lower review scores, but the relationship is not strong.

---

## 4. 📦 Product Category Performance

Product categories are evaluated based on:

* Order volume
* Revenue
* Review scores
* Freight value

### 🏆 Highest-Revenue Category

**Health & Beauty**

### 📦 Highest-Order-Volume Category

**Bed & Bath Table**

Other major categories include:

* Watches & Gifts
* Sports & Leisure
* Computers & Accessories
* Furniture & Decor

### ⚠️ Lowest-Rated Category

Among categories with at least 100 orders:

**Office Furniture — 3.62 / 5**

This category also has relatively high average freight of approximately **R$53.95**, making it an important area for further operational investigation.

---

## 5. 💳 Payment Behavior

Payment activity is dominated by **credit cards**.

### Payment Method Overview

| Payment Method  | Key Observation               |
| --------------- | ----------------------------- |
| **Credit Card** | Most widely used              |
| **Boleto**      | Second-largest payment method |
| **Debit Card**  | Lower order volume            |
| **Voucher**     | Lowest average order value    |

Credit-card orders account for approximately:

* **76,504 orders**
* **R$12.74 million** in recorded revenue

### Average Order Value

| Payment Method | Average Order Value |
| -------------- | ------------------: |
| Credit Card    |        **R$166.47** |
| Boleto         |        **R$145.03** |
| Debit Card     |        **R$142.73** |
| Voucher        |        **R$114.39** |

Payment-related variables show only **weak relationships with customer review scores**, suggesting that payment behavior is considerably less associated with satisfaction than delivery performance.

---

# 🔍 Root Cause Analysis of Low Review Scores

For the root-cause analysis, **low reviews are defined as review scores of 1 or 2**.

The project compares low-review orders against higher-review orders.

| Metric                |    Low Reviews | Higher Reviews |
| --------------------- | -------------: | -------------: |
| Average Review Score  |       **1.22** |       **4.58** |
| Average Delivery Time | **20.22 days** | **11.44 days** |
| On-Time Delivery Rate |     **56.09%** |     **94.77%** |

### Correlation with Review Score

The strongest relationships identified are:

| Factor                          | Correlation with Review Score |
| ------------------------------- | ----------------------------: |
| **On-Time Delivery**            |                    **+0.446** |
| **Delivery Time**               |                    **-0.334** |
| **Delivery Delay**              |                    **-0.267** |
| Order-Item Count                |                    **-0.116** |
| Freight Value                   |                    **-0.089** |
| Payment / Order Value Variables |                 **Very Weak** |

### 🔑 Main Insight

> **On-time delivery has the strongest relationship with customer review score among the analyzed variables.**

This reinforces **delivery reliability as the primary operational area requiring attention**.

---

# 💡 Key Findings

### ⭐ 1. Delivery Is the Strongest Customer-Experience Signal

Late deliveries are strongly associated with lower customer review scores.

### 🚚 2. Severe Delays Have a Major Impact

Average reviews decline from approximately **4.3 for early deliveries** to approximately **1.7 for orders more than 15 days late**.

### 📈 3. Marketplace Activity Grew Substantially

Order volume and revenue generally increased from **2017 into 2018**.

### 🏪 4. Seller Activity Is Geographically Concentrated

**São Paulo** is the dominant seller and customer market.

### 📦 5. Product Category Performance Varies Considerably

**Health & Beauty** leads revenue, while **Bed & Bath Table** leads order volume.

### ⚠️ 6. Office Furniture Requires Investigation

It has the **lowest average review score among categories with at least 100 orders**.

### 💳 7. Credit Cards Dominate Payments

Credit cards represent the largest payment method by both **order count and recorded revenue**.

### 🔍 8. Payment Variables Are Less Important for Satisfaction

Payment-related metrics show considerably weaker relationships with review scores than delivery-related metrics.

---

# 📋 Business Recommendations

## 1. 🚚 Prioritize Late-Delivery Reduction

Monitor orders approaching their estimated delivery dates and intervene before they become late.

Potential operational actions include:

* Proactive shipment monitoring
* Exception alerts
* Seller performance tracking
* Logistics escalation
* Delivery-risk monitoring

---

## 2. 📊 Make Delivery Performance a Core CX KPI

Regularly monitor:

* On-time delivery rate
* Average delivery time
* Delivery delay
* Review score by delivery group

This allows the business to identify deteriorating customer experience early.

---

## 3. 📦 Prioritize High-Volume & High-Revenue Areas

Operational improvements should initially focus on **categories and regions with significant marketplace activity**.

Improving performance in high-volume areas can positively influence a larger portion of the overall customer experience.

---

## 4. 💰 Investigate High-Freight / Low-Rating Segments

Freight cost has only a weak overall relationship with review scores. However, combinations of:

> **High freight + poor reviews**

may indicate specific logistics or customer-experience issues that warrant further investigation.

---

## 5. 💳 Maintain Payment Flexibility

Credit cards dominate payment behavior, but multiple payment methods should continue to be supported.

Payment methods and installment levels should be monitored alongside:

* Order value
* Customer experience
* Conversion
* Review performance

---

## 6. 📊 Build a Recurring Marketplace Dashboard

A recurring management dashboard should monitor:

```text
Orders
Revenue
Average Review Score
On-Time Delivery Rate
Average Delivery Time
Delivery Delay
Freight Value
Category Performance
Geographic Performance
Payment Performance
```

This would provide management with a consistent view of marketplace health and customer experience.

---

# 🏁 Conclusion

The Olist dataset provides a comprehensive view of Brazilian marketplace activity across **orders, products, payments, sellers, customers, delivery, and reviews**.

The analysis demonstrates that:

> **Delivery performance is the dominant operational theme associated with customer satisfaction.**

The strongest signals identified are:

* **Higher on-time delivery → higher review scores**
* **Longer delivery times → lower review scores**
* **Larger delivery delays → substantially lower review scores**
* **Payment behavior → comparatively weak relationship with satisfaction**

From a business perspective, Olist should therefore prioritize:

**delivery reliability, proactive logistics monitoring, and targeted investigation of high-risk categories and regions.**

Overall, the project provides a **data-driven framework for monitoring marketplace performance and identifying opportunities to improve customer experience**.

---

# 📌 Project Highlights

| Metric                                       |       Result |
| -------------------------------------------- | -----------: |
| 🛒 **Orders Analyzed**                       |   **99,441** |
| 💰 **Recorded Payment Value**                | **R$16.01M** |
| ⭐ **Average Review Score**                   | **4.09 / 5** |
| 🚚 **On-Time Delivery Rate**                 |   **89.15%** |
| 📦 **Early Delivery Review Score**           | **4.30 / 5** |
| ⚠️ **Review Score for 15+ Day Delays**       | **1.71 / 5** |
| 🔗 **On-Time Delivery ↔ Review Correlation** |   **+0.446** |

---

# 👤 Author

### **Saikat Pradhan**

**Data Analytics | Python | Exploratory Data Analysis**

---

⭐ **If you found this project useful, consider giving the repository a star!**
