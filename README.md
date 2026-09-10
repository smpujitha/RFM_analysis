

##  Project Overview

This project focuses on **Customer Segmentation and Retention Analysis** using **RFM (Recency, Frequency, Monetary) Analysis** and **Cohort Analysis**.

The objective is to understand:

- Customer purchasing behavior
- Customer value
- Purchase frequency
- Customer retention patterns
- High-value and low-value customer groups
- Customer lifecycle behavior
- Product sales patterns
- Revenue concentration

RFM analysis is used to segment customers based on their purchasing behavior, while Cohort Analysis is used to understand how customer retention changes over time.

The project also applies **K-Means clustering** to identify natural customer groups and provides actionable business recommendations based on the analysis.

---

#  Project Objectives

The main objectives of this project are:

1. Understand customer purchasing behavior.
2. Analyze customer recency, frequency, and monetary value.
3. Segment customers based on their RFM scores.
4. Identify high-value and loyal customers.
5. Identify inactive and at-risk customers.
6. Analyze customer retention using Cohort Analysis.
7. Apply clustering to identify natural customer groups.
8. Identify important products and sales patterns.
9. Analyze unusual and return-related transactions.
10. Provide actionable business recommendations.
11. Help businesses improve customer retention and customer lifetime value.

---

#  Problem Statement

Businesses have large amounts of customer transaction data, but raw transaction records do not directly show which customers are valuable, loyal, inactive, or likely to stop purchasing.

A business needs to understand:

- Which customers purchase recently?
- Which customers purchase frequently?
- Which customers generate the most revenue?
- Which customers are becoming inactive?
- How well are new customers being retained?
- Which customer segments require different marketing strategies?

### Problem:

> **To develop a customer segmentation and retention analysis system using RFM and Cohort Analysis to identify customer value, purchasing behavior, and retention trends, enabling businesses to make better customer relationship and marketing decisions.**

---

#  Approach / Methodology

The project follows the workflow below:

```text
Customer Transaction Dataset
          ↓
Data Understanding
          ↓
Data Cleaning
          ↓
Exploratory Data Analysis
          ↓
Customer Purchase Analysis
          ↓
RFM Calculation
          ↓
RFM Scoring
          ↓
Customer Segmentation
          ↓
K-Means Clustering
          ↓
Cohort Analysis
          ↓
Retention Analysis
          ↓
Product & Sales Analysis
          ↓
Key Insights
          ↓
Business Solutions
          ↓
Recommendations
````

---

#  1. Data Understanding

The project starts by understanding the customer transaction dataset.

The analysis examines:

* Customer transactions
* Products
* Quantity purchased
* Purchase dates
* Customer IDs
* Country
* Revenue-related information

The dataset is analyzed to understand customer purchasing behavior and product performance.

---

#  2. Data Cleaning

Data preprocessing is performed before customer segmentation and analysis.

The cleaning process focuses on:

* Identifying missing values
* Handling invalid records
* Examining unusual quantities
* Identifying negative quantities
* Removing or handling inappropriate transaction records where required
* Preparing transaction data for customer-level analysis

Negative quantities are particularly important because they can represent **returns or cancellations**.

The analysis identifies products with negative quantities and highlights them for further investigation.

---

#  3. Exploratory Data Analysis

Exploratory Data Analysis is performed to understand the dataset and identify important patterns.

The analysis includes:

* Customer purchase frequency
* Product sales quantity
* Product popularity
* Transaction patterns
* Customer purchasing behavior
* Country-wise transaction patterns
* Outlier customers
* Return/cancellation patterns

---

#  Product Analysis

The project analyzes the most frequently purchased and highest-volume products.

One of the frequently purchased products identified is:

**White Hanging Heart T-Light Holder**

Other popular products include:

* Jumbo Bag Red Retrospot
* Regency Cakestand 3 Tier
* Rose Cottage Tea Cup & Saucer

The concentration of purchases around a small number of products indicates that certain products have strong demand.

These products can therefore be prioritized for:

* Inventory management
* Promotions
* Cross-selling
* Product bundles

---

#  High-Volume Product Analysis

The analysis identifies products with high total quantities sold.

**World War 2 Gliders Asstd Designs** has the highest total quantity sold in the analysis.

Other strong products include:

* Jumbo Bag Red Retrospot
* Assorted Colour Bird Ornament

High-volume products should be closely monitored to avoid stock-outs.

They can also be used in:

* Bundle offers
* Cross-selling
* Promotional campaigns

---

#  Low-Sales & Negative Quantity Analysis

Several products have very low sales quantities.

The dataset also contains negative quantities, which may indicate:

* Product returns
* Order cancellations
* Refund-related transactions

**Rotating Silver Angels T-Light Holder** has a particularly large negative quantity.

Products with consistently low demand may require:

* Reduced inventory
* Promotional campaigns
* Product evaluation

Products with unusually high negative quantities should be investigated to understand return-related issues.

---

#  4. RFM Analysis

RFM stands for:

```text
R → Recency
F → Frequency
M → Monetary
```

RFM Analysis is used to measure customer value based on purchasing behavior.

---

## Recency

Recency measures:

> **How recently a customer made a purchase.**

Customers with more recent purchases are generally more engaged.

A customer who purchased recently is more likely to be active compared with a customer who has not purchased for a long time.

---

##  Frequency

Frequency measures:

> **How often a customer makes purchases.**

Customers with high purchase frequency may represent loyal or highly engaged customers.

The analysis identifies a small group of customers with significantly higher transaction frequency than others.

Customer **17841** is identified as the most frequent customer in the analysis.

High-frequency customers can be considered potential loyal or high-value customers.

---

##  Monetary

Monetary value measures:

> **How much money a customer has spent.**

Customers with high monetary values contribute significantly to business revenue.

These customers should be protected through appropriate retention and loyalty strategies.

---

#  5. RFM Score Calculation

Customers are assigned scores based on:

* Recency
* Frequency
* Monetary value

These scores help categorize customers into meaningful customer segments.

The RFM framework allows the business to distinguish between:

* High-value customers
* Loyal customers
* Potential loyalists
* At-risk customers
* Lost customers
* Low-value customers

---

#  Customer Segmentation

RFM analysis identifies different customer segments based on their purchasing behavior.

Important segments include:

### Champions

Highly engaged and valuable customers who purchase recently and frequently.

### Potential Loyalists

Customers showing good purchasing behavior who may become highly loyal customers.

### At Risk

Customers who were previously active but have not purchased recently.

### Lost Customers

Customers with very low recent engagement and long periods since their last purchase.

These segments allow businesses to use different strategies instead of treating every customer equally.

---

#  6. K-Means Clustering

K-Means clustering is used to identify natural customer groups based on customer behavior.

The analysis identifies **3 major customer groups**:

| Cluster              | Customer Count | General Description                    |
| -------------------- | -------------: | -------------------------------------- |
| Low-value / Inactive |          1,545 | Less active and lower-value customers  |
| Mid-value            |          1,843 | Moderate purchasing activity and value |
| High-value / Loyal   |            984 | Highly engaged and valuable customers  |

The clustering results support the segmentation obtained through RFM analysis.

---

#  7. Cohort Analysis

Cohort Analysis is used to study **customer retention over time**.

Customers are grouped into cohorts based on their initial purchase period.

The analysis then tracks how many customers from each cohort continue purchasing in subsequent months.

This helps answer:

* Do customers return after their first purchase?
* How quickly does retention decline?
* Which cohorts perform better?
* Where does customer drop-off occur?

---

#  Customer Retention Analysis

A major finding from the Cohort Analysis is that:

> **Customer retention drops sharply after the first month.**

Across almost every cohort, retention decreases from the initial month to approximately **20–40% by the second month**.

This indicates a significant early-stage customer retention challenge.

Therefore, businesses should focus strongly on the period immediately following the customer's first purchase.

---

#  Country Analysis

The analysis shows that the **UK accounts for the large majority of transactions**.

However, retention quality varies across different cohort months.

This indicates that geographical customer behavior can also be considered when designing customer retention strategies.

---

#  High-Value Customer Analysis

Customer value is highly concentrated among a smaller group of highly engaged customers.

The analysis identifies a **Champions** segment with approximately:

```text
Recency ≈ 14 days
Frequency ≈ 272
Average Spend ≈ $6,197
```

In comparison, Lost Customers have an average spend of approximately:

```text
$127
```

This large difference demonstrates why identifying high-value customers is important.

---

#  Outlier Customer Analysis

The analysis identifies a small number of customers with exceptionally high lifetime spending.

There are **9 major outlier customers**, each carrying six-figure lifetime spending levels.

These customers represent extremely valuable accounts and require special attention.

---

#  Key Insights

The major findings from the analysis are:

### 1. Customer value is highly concentrated

A relatively small group of highly engaged customers generates a significant amount of customer value.

### 2. Champions are highly valuable

The Champions segment has approximately $6,197 average spend compared with approximately $127 for Lost Customers.

### 3. Retention drops after the first month

Cohort Analysis shows a major decrease in customer retention after the initial purchase period.

### 4. Three major customer groups exist

K-Means clustering identifies:

* Low-value / inactive customers
* Mid-value customers
* High-value / loyal customers

### 5. Some customers generate extremely high revenue

Nine major outlier customers have exceptionally high lifetime spending.

### 6. Product demand is concentrated

A relatively small number of products account for a large amount of purchasing activity.

### 7. Returns and cancellations require attention

Negative quantity records indicate potential product returns or cancellations.

### 8. UK dominates transactions

The UK contributes the majority of transactions in the analyzed dataset.

---

#  Business Solution

The proposed business solution is:

```text
Customer Transaction Data
          ↓
RFM Analysis
          ↓
Customer Segmentation
          ↓
K-Means Clustering
          ↓
Cohort Retention Analysis
          ↓
Identify Customer Value
          ↓
Identify At-Risk Customers
          ↓
Targeted Marketing Strategies
          ↓
Customer Retention
          ↓
Increase Customer Lifetime Value
```

The combination of RFM and Cohort Analysis allows businesses to understand both:

**Customer Value → RFM**

and

**Customer Retention → Cohort Analysis**

Together, these analyses provide a more complete view of customer behavior.

---

#  Actionable Business Solutions

## 1. Launch a Loyalty / VIP Program

Champions and high-value customers should receive:

* Loyalty rewards
* VIP benefits
* Personalized offers
* Early access to products
* Exclusive promotions

This helps protect the high-value customer segment.

---

## 2. Win-Back Campaigns

Customers classified as **At Risk** or **Lost** can be targeted using automated campaigns.

Possible strategies include:

* Personalized discounts
* Product recommendations
* Special offers
* Reminder emails
* Limited-time promotions

Customers with very high recency values, such as those inactive for more than 150 days, can be prioritized.

---

## 3. Improve Post-Purchase Engagement

Since retention drops sharply after the first month, businesses should strengthen the customer experience immediately after the first purchase.

Possible strategies:

* Welcome campaigns
* Follow-up emails
* Product recommendations
* Loyalty-point incentives
* Second-purchase discounts

The goal is to encourage customers to make another purchase before they become inactive.

---

## 4. Dedicated Account Management

The 9 extremely high-value outlier customers should receive additional attention.

Businesses can provide:

* Dedicated account support
* Personalized communication
* Premium services
* Exclusive offers
* Priority customer service

This helps protect customers who contribute exceptionally high lifetime value.

---

## 5. Upselling & Cross-Selling

Potential Loyalists and mid-value customers can be targeted with:

* Related products
* Product bundles
* Personalized recommendations
* Premium product upgrades
* Cross-selling offers

The goal is to move these customers toward the high-value/loyal segment.

---

## 6. Inventory Optimization

Best-selling products should be monitored carefully.

Businesses can:

* Maintain sufficient stock
* Predict demand
* Create product bundles
* Promote complementary products
* Avoid stock-outs

Low-demand products can be evaluated for discounts or reduced inventory.

---

## 7. Analyze Product Returns

Products with unusually high negative quantities should be investigated.

Businesses can examine:

* Return reasons
* Product quality
* Customer complaints
* Shipping problems
* Product descriptions

This can help reduce unnecessary returns and improve customer satisfaction.

---

#  Business Benefits

The project can help businesses:

* Improve customer retention
* Identify high-value customers
* Reduce customer loss
* Increase customer lifetime value
* Personalize marketing campaigns
* Improve customer engagement
* Identify inactive customers
* Improve product promotions
* Optimize inventory
* Reduce unnecessary returns
* Improve cross-selling opportunities
* Support data-driven decision making

---

# 📊 Project Outcome

The project combines:

```text
RFM Analysis
      +
K-Means Clustering
      +
Cohort Analysis
      +
Product Analysis
      =
Customer Segmentation & Retention Strategy
```

The analysis provides businesses with a better understanding of:

* Who their most valuable customers are
* Who is becoming inactive
* How customers behave over time
* Which products are most important
* Where retention problems occur
* Which customers require targeted marketing

---

#  Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook


#  Future Enhancements

The project can be extended by:

* Developing an automated customer segmentation dashboard
* Creating real-time RFM scoring
* Adding customer churn prediction
* Building a recommendation system
* Automating email/SMS campaigns
* Adding interactive Power BI/Tableau dashboards
* Using advanced clustering algorithms
* Creating customer lifetime value prediction
* Integrating the system with CRM platforms
* Building a web-based customer analytics application

---

#  Conclusion

This project demonstrates how **RFM Analysis, Cohort Analysis, and K-Means Clustering** can be combined to understand customer value, purchasing behavior, and retention.

The analysis shows that customer value is concentrated among a smaller group of highly engaged customers, while customer retention drops significantly after the initial purchase period.

Therefore, businesses should focus on:

* Protecting high-value customers
* Reactivating at-risk and lost customers
* Improving post-first-purchase engagement
* Using personalized marketing
* Optimizing inventory around best-selling products
* Investigating return-related issues

Overall, the project demonstrates how customer transaction data can be transformed into **actionable customer segmentation and retention strategies**.


```
