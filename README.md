# Retail Sales Analysis Using Oracle SQL

## 1. Business Problem

Retail companies generate large volumes of transactional sales data across customers, products, regions, and time periods.  
However, without proper analysis, it is difficult for management to understand product performance, customer behavior, and sales trends.

This project addresses the challenge of transforming raw sales data into meaningful business insights using **SQL JOINs and Window Functions**.  
The analysis supports decision-making in areas such as marketing strategy, customer segmentation, inventory management, and sales forecasting.



## 2. Database Schema and ER Diagram

### 2.1 Schema Description

The database consists of three main tables:

- **CUSTOMERS**: Stores customer details and regions  
- **PRODUCTS**: Stores product information and pricing  
- **SALES**: Stores transactional sales records

### Tables Overview

**CUSTOMERS**
- customer_id (PK)
- first_name
- last_name
- region

**PRODUCTS**
- product_id (PK)
- product_name
- price

**SALES**
- sale_id (PK)
- - sale_date
- quantity
- customer_id (FK)
- product_id (FK)


### 2.2 ER Diagram

- One customer can make multiple sales  
- One product can appear in multiple sales  
- The SALES table resolves the many-to-many relationship between customers and products  


## 3. SQL JOIN Queries

SQL JOINs were used to combine data from multiple tables and answer business questions.

### JOIN Types Implemented
- **INNER JOIN**: Retrieve valid sales transactions involving existing customers and products  
- **LEFT JOIN**: Identify customers with no purchase history  
- **RIGHT / LEFT JOIN (Products)**: Identify products that have never been sold  
- **FULL OUTER JOIN**: Display all customers and products, including unmatched records  
- **SELF JOIN**: Compare customers within the same region  

These JOINs help the business analyze customer activity, product performance, and data completeness.



## 4. Window Function Queries

Window functions were used to perform advanced analytical operations without collapsing result sets.

### 4.1 Ranking Function (RANK)
Ranks products based on total quantity sold to identify top-performing products.

### 4.2 Aggregation Function (SUM() OVER)
Calculates running totals of sales to analyze cumulative growth over time.

### 4.3 Navigation Function (LAG)
Compares current period sales with previous period sales to detect trends and changes.

### 4.4 Distribution Function (NTILE)
Segments customers into quartiles based on purchasing volume for targeted marketing.

All queries are written using **Oracle SQL** and are included in the repository.



## 5. Key Business Insights

- High-performing products were identified using ranking analysis, enabling better inventory and promotion decisions  
- Running totals revealed overall sales growth trends across time periods  
- Month-over-month comparison highlighted periods of sales increase and decline  
- Customer segmentation identified high-value customers suitable for loyalty programs  
- Inactive customers and unsold products were detected, supporting marketing and product strategy adjustments  


## 6. References

1. Oracle Corporation. *Oracle Database SQL Language Reference*  
2. Oracle Corporation. *Analytic Functions Documentation*  
3. Silberschatz, A., Korth, H. F., & Sudarshan, S. *Database System Concepts*  
4. Lecture Notes – Database Management Systems  



## 7. Academic Integrity Statement

I declare that this project is my original work and has been completed in accordance with academic integrity guidelines.  
All external sources used have been properly referenced, and no part of this work has been copied or plagiarized.




