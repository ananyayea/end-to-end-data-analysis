# Customer Shopping Behavior Analysis

## Project Overview

This project analyzes customer shopping behavior using transactional
data from **3,900 purchases** across different product categories. The
objective is to identify patterns in customer spending, customer
segments, product preferences, discount usage, shipping choices, and
subscription behavior to support data-driven business decisions.

## Dataset Summary

-   **Rows:** 3,900
-   **Columns:** 18
-   **Missing Data:** 37 missing values in the `Review Rating` column

### Main Dataset Features

-   **Customer Demographics:** Age, Gender, Location, Subscription
    Status
-   **Purchase Details:** Item Purchased, Category, Purchase Amount,
    Season, Size, Color
-   **Shopping Behavior:** Discount Applied, Promo Code Used, Previous
    Purchases, Frequency of Purchases, Review Rating, Shipping Type

## Tools and Technologies

-   Python
-   Pandas
-   NumPy
-   PostgreSQL
-   SQL
-   Power BI
-   Jupyter Notebook

## Project Workflow

``` text
Raw Dataset
    ↓
Data Cleaning and Preparation using Python
    ↓
Feature Engineering
    ↓
PostgreSQL Database Integration
    ↓
SQL-Based Business Analysis
    ↓
Interactive Power BI Dashboard
    ↓
Business Insights and Recommendations
```

## Data Preparation Using Python

The following tasks were performed:

-   Loaded the dataset using Pandas.
-   Explored the dataset using `info()` and `describe()`.
-   Checked for missing values.
-   Imputed missing `Review Rating` values using the median rating of
    the corresponding product category.
-   Renamed columns into `snake_case` format.
-   Created an `age_group` column by grouping customers according to
    age.
-   Created a `purchase_frequency_days` feature from purchase data.
-   Checked whether `discount_applied` and `promo_code_used` were
    redundant.
-   Removed the redundant `promo_code_used` column.
-   Connected Python to PostgreSQL.
-   Loaded the cleaned DataFrame into PostgreSQL for SQL analysis.

## SQL Business Analysis

PostgreSQL was used to answer these business questions:

1.  How does total revenue compare between male and female customers?
2.  Which customers used discounts but still spent more than the average
    purchase amount?
3.  Which five products have the highest average review ratings?
4.  How do average purchase amounts compare between Standard and Express
    shipping?
5.  How do subscribers and non-subscribers compare in average spending
    and total revenue?
6.  Which five products have the highest percentage of discounted
    purchases?
7.  How can customers be classified as New, Returning, or Loyal based on
    purchase history?
8.  What are the top three most-purchased products in each category?
9.  Are customers with more than five purchases more likely to
    subscribe?
10. Which age groups contribute the most revenue?

## Power BI Dashboard

An interactive Power BI dashboard was created to present the analysis
visually. It helps explore:

-   Customer and revenue patterns
-   Subscription behavior
-   Product performance
-   Discount usage
-   Customer segments
-   Shipping preferences
-   Revenue contributions by age group

## Business Recommendations

-   **Boost Subscriptions:** Promote exclusive benefits for subscribers.
-   **Develop Loyalty Programs:** Reward repeat buyers and encourage
    customers to become Loyal customers.
-   **Review Discount Policies:** Balance discount-driven sales growth
    with profit-margin control.
-   **Improve Product Positioning:** Promote top-rated and best-selling
    products in marketing campaigns.
-   **Use Targeted Marketing:** Focus on high-revenue age groups and
    customers who prefer express shipping.

## Project Structure

``` text
customer-shopping-behavior-analysis/
│
├── Python/
│   └── customer_shopping_behavior.ipynb
│
├── SQL/
│   └── business_analysis_queries.sql
│
├── PowerBI/
│   └── customer_behavior_dashboard.pbix
│
├── Screenshots/
│   └── dashboard.png
│
└── README.md
```

> Update the file names and folders according to the files included in
> your repository.

## How to Run the Project

### 1. Clone the Repository

``` bash
git clone <your-repository-link>
cd customer-shopping-behavior-analysis
```

### 2. Install Python Libraries

``` bash
pip install pandas numpy jupyter psycopg2-binary
```

### 3. Run the Python Analysis

-   Open the Python notebook in Jupyter Notebook.
-   Update the dataset path if required.
-   Run the notebook cells in sequence.

### 4. Run the SQL Analysis

-   Set up a PostgreSQL database.
-   Load the cleaned dataset into PostgreSQL.
-   Execute the SQL queries in the SQL folder.

### 5. Open the Power BI Dashboard

-   Open the `.pbix` file in Power BI Desktop.
-   Update the data source or database connection if required.
-   Refresh the data.

## Conclusion

This project demonstrates an end-to-end data analytics workflow,
beginning with data cleaning and feature engineering in Python, followed
by business-focused SQL analysis in PostgreSQL and interactive
visualization in Power BI.

It shows how customer transaction data can be transformed into
meaningful insights and practical business recommendations.


