# RFM_analysis 
````markdown
# RFM and Cohort Analysis for Customer Segmentation and Retention

## 1. Project Overview

This project focuses on analyzing customer purchasing behavior using **RFM (Recency, Frequency, Monetary) Analysis**, **K-Means Clustering**, and **Cohort Analysis**.

The main objective is to understand:

- Customer purchasing behavior
- Customer value
- Different customer segments
- High-value and inactive customers
- Customer retention patterns over time
- How Machine Learning can be used for customer segmentation

The analysis was performed using an Online Retail transaction dataset.

---

## 2. Problem Statement

Businesses have a large amount of customer transaction data, but raw transaction data does not directly explain which customers are valuable, which customers are inactive, or how customer retention changes over time.

This project uses RFM Analysis and Cohort Analysis to convert transaction data into useful customer insights.

K-Means Clustering is additionally used as an unsupervised Machine Learning technique to identify groups of customers with similar purchasing behavior.

---

## 3. Objectives

The main objectives of this project are:

1. Clean and preprocess the retail transaction dataset.
2. Perform Exploratory Data Analysis (EDA).
3. Calculate Recency, Frequency, and Monetary values.
4. Assign RFM scores to customers.
5. Segment customers based on their RFM scores.
6. Apply K-Means clustering for customer segmentation.
7. Use the Elbow Method to determine a suitable number of clusters.
8. Perform Cohort Analysis.
9. Calculate customer retention rates.
10. Identify customer behavior and retention patterns.
11. Provide useful business recommendations.

---

## 4. Dataset

The project uses an Online Retail transaction dataset.

The important columns used in the analysis include:

- **InvoiceNo** – Invoice/transaction number
- **StockCode** – Product code
- **Description** – Product description
- **Quantity** – Number of products purchased
- **InvoiceDate** – Date and time of transaction
- **UnitPrice** – Price per product
- **CustomerID** – Unique customer identifier
- **Country** – Customer's country

---

## 5. Technologies and Libraries Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

---

# 6. Data Preprocessing

The following preprocessing steps were performed:

### Missing Values

Missing values were checked using Pandas.

Customer-related missing values were handled because CustomerID is required for customer-level analysis.

### Duplicate Values

Duplicate records were checked and removed to avoid repeated transactions affecting the analysis.

### Date Conversion

The InvoiceDate column was converted into a datetime format to perform date-based calculations.

### Total Amount

A new feature called `TotalSum` was created:

```python
TotalSum = Quantity * UnitPrice
````

This value represents the total amount associated with a transaction.

---

# 7. Exploratory Data Analysis

Basic EDA was performed to understand the dataset and customer behavior.

The project includes visualizations such as:

* Top 10 countries by transactions
* Correlation heatmap
* Customer-related analysis
* Purchase behavior analysis

These visualizations provide an initial understanding of the dataset before performing RFM and Cohort Analysis.

---

# 8. RFM Analysis

RFM Analysis is used to understand customer value based on three important metrics.

### Recency

Recency measures how recently a customer made a purchase.

A lower Recency value means the customer purchased more recently.

### Frequency

Frequency measures how many transactions a customer has made.

A higher Frequency indicates that the customer purchases more frequently.

### Monetary

Monetary value measures how much money a customer has spent.

A higher Monetary value indicates a higher-value customer.

---

## RFM Calculation

The RFM table was created at customer level using:

* Recency
* Frequency
* MonetaryValue

The customer transaction data was grouped using `groupby()` to calculate these metrics.

---

# 9. RFM Scoring

RFM scores were assigned using `pd.qcut()`.

The values were divided into five quantile-based groups and assigned scores from 1 to 5.

For Recency:

* Lower Recency = better score
* Higher Recency = lower score

For Frequency and Monetary:

* Higher value = better score
* Lower value = lower score

The individual R, F and M scores were combined to create an overall RFM score.

---

# 10. Customer Segmentation

Customers were segmented based on their overall RFM score.

The project uses segments such as:

* Champions
* Loyal Customers
* Potential Loyalists
* At Risk
* Lost Customers

These segments help businesses understand customer value and purchasing behavior.

For example:

### Champions

Customers with strong Recency, Frequency and Monetary behavior.

### Loyal Customers

Customers who regularly purchase and provide good customer value.

### Potential Loyalists

Customers who show potential to become more valuable customers.

### At Risk

Customers who have not purchased recently and may require re-engagement.

### Lost Customers

Customers with weak recent purchasing activity and low overall engagement.

---

# 11. K-Means Clustering

K-Means Clustering was used as an additional Machine Learning technique.

K-Means is an **unsupervised Machine Learning algorithm** that groups similar observations into clusters.

For this project, the following RFM features were used:

* Recency
* Frequency
* MonetaryValue

The features were scaled using `StandardScaler()` because the variables have different ranges.

---

# 12. Elbow Method

The Elbow Method was used to determine a suitable number of clusters.

Different values of K were tested and their inertia values were compared.

**Inertia** measures how close the observations are to the centroid of their assigned cluster.

As the number of clusters increases, inertia generally decreases.

The point where the improvement begins to reduce significantly is considered the elbow point.

Based on the analysis, **K = 5** was selected for the K-Means model.

---

# 13. K-Means Cluster Analysis

After applying K-Means, customers were divided into five clusters.

The clusters were analyzed using their average:

* Recency
* Frequency
* MonetaryValue

The analysis showed that different clusters have different purchasing behaviors.

Some clusters contain highly active and high-value customers, while another cluster contains customers with high Recency and comparatively lower Frequency and Monetary value.

This allows businesses to understand customer groups using a data-driven Machine Learning approach.

---

# 14. Cohort Analysis

Cohort Analysis is used to understand customer retention over time.

Customers were grouped into cohorts based on the month of their first purchase.

A **Cohort Month** was created to identify when customers first joined the business.

A **Cohort Index** was then calculated to identify how many months had passed since the customer's first purchase.

---

# 15. Retention Analysis

Retention rates were calculated for each customer cohort.

A retention table was created to understand how many customers continued purchasing in subsequent months.

A heatmap was used to visualize the retention rates.

The heatmap helps identify:

* Strong customer retention
* Decreasing retention over time
* Differences between customer cohorts
* Customer loyalty patterns

---

# 16. Key Business Insights

### Customer Value

RFM Analysis shows that customers have different purchasing behaviors based on Recency, Frequency and Monetary value.

Customers with recent purchases, higher purchase frequency and higher spending represent valuable customer groups.

### Customer Segmentation

RFM segmentation separates customers into groups such as Champions, Loyal Customers, Potential Loyalists, At Risk and Lost Customers.

This allows businesses to create different strategies for different customer groups.

### K-Means Clustering

K-Means clustering identified five groups of customers with different RFM characteristics.

The clusters showed differences in customer activity, purchasing frequency and monetary value.

### High-Value Customers

Customers with low Recency, high Frequency and high Monetary value represent highly active and valuable customers.

### Inactive Customers

Customers with high Recency and relatively low Frequency and Monetary value appear less engaged and may require reactivation strategies.

### Retention

Cohort Analysis provides an understanding of how customer retention changes over time and helps identify patterns in customer loyalty.

---

# 17. Business Recommendations

### 1. Reward High-Value Customers

Businesses can provide loyalty rewards, exclusive offers and personalized promotions to high-value customers.

### 2. Re-engage At-Risk Customers

Customers with high Recency and low purchasing activity can be targeted using personalized offers, reminders and reactivation campaigns.

### 3. Improve Customer Retention

Businesses can improve retention through better post-purchase communication, customer service and loyalty programs.

### 4. Personalized Marketing

Different RFM segments and K-Means clusters can be targeted with different marketing strategies instead of treating all customers equally.

### 5. Focus on High-Value Customer Groups

Businesses should focus on retaining customers who purchase frequently and spend more because these customers contribute significantly to revenue.

---

# 18. Project Workflow

The overall workflow of the project is:

```text
Raw Transaction Data
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Feature Engineering
        ↓
       RFM
        ↓
RFM Scoring
        ↓
Customer Segmentation
        ↓
K-Means Clustering
        ↓
Elbow Method
        ↓
5 Customer Clusters
        ↓
Cohort Analysis
        ↓
Retention Analysis
        ↓
Business Insights
        ↓
Business Recommendations
```

---

# 19. Conclusion

This project combines **RFM Analysis, K-Means Clustering and Cohort Analysis** to understand customer value, purchasing behavior and retention patterns.

RFM Analysis provides a simple method for segmenting customers based on their purchasing behavior, while K-Means provides a Machine Learning approach to identify naturally occurring customer groups.

Cohort Analysis helps businesses understand how customer retention changes over time.

Overall, the analysis can help businesses identify valuable customers, recognize inactive or at-risk customers, improve retention strategies and create targeted marketing campaigns.

---



---

# 22. Final Outcome

The project demonstrates how customer transaction data can be transformed into meaningful business insights using:

* Data Cleaning
* Exploratory Data Analysis
* RFM Analysis
* Customer Segmentation
* Unsupervised Machine Learning
* K-Means Clustering
* Cohort Analysis
* Retention Analysis
* Data Visualization


```
