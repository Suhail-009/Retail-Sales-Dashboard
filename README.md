📊 **Retail Sales Analysis – Power BI Dashboard**

📁 **Project Overview:**

This Power BI dashboard provides a complete analysis of Retail Sales for the year 2024, including category performance, customer insights, profitability, and monthly trends.
The dashboard is fully interactive with slicers for Year, Month Name, and Gender, allowing users to dynamically explore retail performance.

🎯 **Key Objectives:**

* Track overall sales performance
* Identify high-profit categories
* Analyze buying behavior across gender and months
* Understand average selling price trends
* Review customer-level sales contributions


🖼 **Dashboard Preview:**
![Retail-Sales-Dashboard](dashboard.png)


📌 **Dashboard Components:**

🟨 **1. Total Sales KPI:**

Shows the overall revenue generated after all applied filters (e.g., month, gender). 

**Value shown in dashboard:** 88.39K

🟨 **2. Total Profit KPI:**

Displays the net profit after subtracting COGS (Cost of Goods Sold). 

**Value shown in dashboard:** 22.10K

📦 **3. Total Sales by Category (Bar Chart):**

__Visual shows performance across product categories like:__

* Electronics
* Furniture
* Sports
* Clothing
* Cosmetics
* Groceries
* Electronics appears as the highest-selling category.

💰 **4. Profit by Category (Bar Chart):**

Compares profit distribution across categories, highlighting:

* Electronics as the most profitable
* Smaller contributions from Clothing & Cosmetics

👥 **5. Customer-Level Sales Table:**

A detailed table showing:
* Customer ID
* Category purchased
* Total Sales
* Quantity Purchased
* Useful for customer segmentation and high-value customer identification.


📈 **6. Avg Sell Price by Month (Line Chart):**

Shows monthly changes in Average Selling Price (ASP).
Example:
* April shows an ASP around 4.4K.



📅 **7. Total Sales by Year (Card/Scatter):**

Displays annual sales for the selected year.
Example:
* 2024 shows approx 88K in sales.
  


🎛 **8. Interactive Slicers:**

Left-side slicers provide user control:
* Year
* Month Name (January → June)
* Gender (Male / Female)
These automatically update all visuals on the report.
  


🧩 **Dataset Description:**
| Field Name     | Description                |
| -------------- | -------------------------- |
| transaction_id | Unique transaction code    |
| sale_date      | Transaction date           |
| sale_time      | Time of sale               |
| customer_id    | Unique customer identifier |
| gender         | Customer gender            |
| age            | Age of customer            |
| category       | Product category           |
| quantity       | Units in each transaction  |
| price_per_unit | Selling price              |
| cogs           | Cost of goods sold         |
| total_sale     | Final transaction amount   |



🛠 **Data Cleaning & Transformations (Power Query):**

* Converted date from DD-MM-YYYY to actual Date format
* Created Month Name and Year columns
* Removed duplicates and null values
* Corrected data types (numeric, text, date)
* Cleaned category names
* Verified quantity and price calculations


📐 **DAX Measures Used:**

__DAX__
* Total Sales = SUM(retail_sales[total_sale])

* Total Profit = SUM(retail_sales[total_sale]) - SUM(retail_sales[cogs])

* Total Quantity = SUM(retail_sales[quantity])

* Average Selling Price = DIVIDE([Total Sales], [Total Quantity])


📌 **Key Insights:**

* Electronics is the top-performing category both in revenue and profit.
* Profit margin is strongest in high-ticket items like Electronics and Furniture.
* April shows a higher Average Selling Price compared to other months.
* Female customers contribute significantly to sales volume.
* Customer-wise table shows several high-value customers in the Sports category.


🧰**Tools Used:**

* Power BI Desktop
* Power Query
* DAX
* CSV Retail Dataset


🚀 **How to Use This Project:**

* Download the .pbix file from the repository
* Download the dataset (CSV)
* Open the file in Power BI Desktop
* Use slicers to interact with the dashboard
