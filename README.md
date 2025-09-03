# Sales-Insights-Dashboard-MySQL-Power-BI-
---

“Built an end-to-end Sales Insights Dashboard using MySQL and Power BI by preparing data with SQL, creating DAX measures, and developing interactive reports to track KPIs such as revenue, demand, and product performance.”

---

**Prerequisites**
---

MYSQL installed and running.

Power BI Desktop installed.

Sample sales data (e.g., CSV files or database dumps) for testing.

Basic knowledge of SQL and DAX.

---

**Step-by-Step Guide**
---

**Step 1: Understanding the Test Environment Data & Requirements.**

**Step 2: Importing the Data in Test Environment in MYSQL.**

**Step 3: Applying Left Join in MYSQL to Prepare the Data for Reporting.**

**Step 4: Importing the Data to Power BI Desktop from Test Environment.**

**Step 5: Creating the DAX Measures & KPIs for Page 1.**

---

**Step 1: Understanding the Test Environment Data & Requirements.**

Begin by analyzing the sales data and project requirements in a test environment. This ensures the data is suitable for reporting without affecting production systems.

**Key Activities:**

Review the dataset structure: Identify tables such as test, Products.

Common columns might include order_date, product_id, availability, demand, product_id, product_name, unit_price($).

Understand requirements: Define what insights are needed, 

Tips:

Use tools like MySQL Workbench to explore the data.

Document assumptions, such as data types (e.g., datetime for dates, decimal for revenue) and any missing values.

---

**Step 2: Importing the Data in Test Environment in MYSQL.**

Import the raw test data into the MYSQL workbench test environment. If your data originates from MySQL, you can export it as SQL dumps or CSV and import accordingly.

Key Activities:

Create a new database: Use CREATE DATABASE test_env;.

Create tables: Define schemas matching your data, e.g.:

-- Create table
CREATE TABLE test (
    order_date DATE,
    product_id INT,
    availability INT,
    demand INT
);

Tips:

Handle errors like data type mismatches or duplicates.

If using MySQL instead, replace with LOAD DATA INFILE commands.

<img width="405" height="247" alt="image" src="https://github.com/user-attachments/assets/aeaa2e95-e384-4ef6-bbc9-65fcd74fcebe" />

---

**Step 3: Applying Left Join in MYSQL to Prepare the Data for Reporting.**

Refine the data by joining tables to create a comprehensive dataset for reporting. A LEFT JOIN ensures all records from the primary table (e.g., Sales) are included, even if matching data is missing in joined tables.

**Key Activities:**

Identify joins needed: For example, join test with Products for enriched data.

Write the SQL query:

<img width="992" height="120" alt="image" src="https://github.com/user-attachments/assets/264e8852-b8f1-4c6d-9f70-93bd32d7c8d0" />

Create a view or materialized table: Save the joined result for easy access in Power BI.

<img width="482" height="352" alt="image" src="https://github.com/user-attachments/assets/f8bbf205-f44b-46cb-b498-5a3efaac9f98" />

Test the query: Ensure no data loss and validate with sample outputs.


**Tips:**

Use LEFT JOIN to preserve all test records; switch to INNER JOIN if complete matches are required.

Optimize for performance if dealing with large datasets (e.g., add indexes on join columns).

---

**Step 4: Importing the Data to Power BI Desktop from Test Environment.**



