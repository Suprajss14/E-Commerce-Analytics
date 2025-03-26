

# **E-commerce Data Analytics Project**  
🚀 **Unlocking Business Insights with Data Analysis**  

## **Overview**  
This project focuses on analyzing e-commerce transaction data using **Python, MySQL, and data visualization tools**. It involves **loading structured data into a database, querying key business metrics, and generating insights** through interactive visualizations.  

## **Tech Stack**  
- **Python** (Pandas, Matplotlib, Seaborn)  
- **MySQL** (Data Storage & Querying)  
- **Jupyter Notebook** (Data Analysis & Visualization)  

## **Project Workflow**  
1. **Data Ingestion:**  
   - Reads multiple **CSV files** (customers, orders, products, payments, etc.).  
   - Stores data in a **MySQL database** (`ecommerce`).  

2. **Data Processing & Analysis:**  
   - Identifies **unique customer locations**.  
   - Calculates **total orders in 2017**.  
   - Analyzes **sales per product category**.  

3. **Visualization & Business Insights:**  
   - Uses **Seaborn & Matplotlib** for **trend analysis and reporting**.  

## **Key SQL Queries Used**  
```sql
-- List all unique customer locations
SELECT DISTINCT customer_city FROM customers;

-- Count total orders in 2017
SELECT COUNT(order_id) FROM orders WHERE YEAR(order_purchase_timestamp) = 2017;

-- Total sales per product category
SELECT p.product_category, ROUND(SUM(pay.payment_value),2) AS sales
FROM products p
JOIN order_items oi ON p.product_id = oi.product_id
JOIN payments pay ON pay.order_id = oi.order_id
GROUP BY p.product_category;
```

## **How to Run the Project**  
1. Install dependencies:  
   ```bash
   pip install pandas mysql-connector-python matplotlib seaborn
   ```
2. Set up MySQL and import the dataset.  
3. Run `csv_to_sql.py` to load data into MySQL.  
4. Open `data analytics.ipynb` for analysis and visualization.  

## **Results & Business Impact**  
✔️ **Customer demographics & location trends**  
✔️ **Sales & revenue insights**  
✔️ **Data-driven recommendations for e-commerce businesses**  


