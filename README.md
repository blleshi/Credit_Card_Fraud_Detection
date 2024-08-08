# Credit Card Fraud Detection Challenge

## Instructions

### Data Modeling

**Step 1: Create an Entity Relationship Diagram (ERD)**
- Inspect the provided CSV files to determine the structure of the data.
- Define how many tables are necessary and the relationships among them.
- Use a tool like Quick Database Diagrams to create your ERD.

**Hints:**
- For the `credit_card` and `transaction` tables, the `card` column should be a `VARCHAR(20)` rather than an `INT`.
- For the `transaction` table, the `date` column should be a `TIMESTAMP` rather than `DATE`.

### Data Engineering

**Step 2: Create a Database Schema**
- Using your ERD as a blueprint, create the database schema.
- Define data types, primary keys, foreign keys, and other constraints for each table.
- Populate the database with data from the corresponding CSV files.

### Data Analysis

**Part 1: Analyze Potential Fraudulent Transactions**

**Step 1: Generate Queries**

1. **Identify Small Transactions:**
   - Isolate transactions less than $2.00 per cardholder.
   - Count the transactions per cardholder.

2. **Evidence of Hacked Credit Cards:**
   - Analyze if there's evidence of hacking based on the number and pattern of small transactions.

3. **High Transactions in Specific Time Frame:**
   - Find the top 100 highest transactions made between 7:00 am and 9:00 am.
   - Identify any anomalous transactions and compare the number of fraudulent transactions during this period versus the rest of the day.

4. **Merchants Prone to Hacking:**
   - Identify the top 5 merchants prone to small transaction hacks.

**Step 2: Create Views for Queries**
- Create views in the database for each query for easy reference and analysis.

**Part 2: Detailed Trends Data for Specific Cardholders**

1. **Important Customers Analysis:**
   - Cardholder IDs 2 and 18: Verify fraudulent transactions.
   - Create a line plot for each cardholder representing the time series of transactions over the year.
   - Create a combined line plot for comparison.

2. **Corporate Credit Card Analysis:**
   - Cardholder ID 25: Analyze suspected unauthorized transactions.
   - Create a box plot of expenditures from January 2018 to June 2018.
   - Identify and analyze outliers and anomalies.

### Challenge: Identifying Fraudulent Transactions

**Step 1: Detect Outliers**

1. **Standard Deviation Method:**
   - Code a Python function to identify anomalies based on standard deviation for any cardholder.

2. **Interquartile Range (IQR) Method:**
   - Code a Python function to identify anomalies based on IQR for any cardholder.

**Reference Articles:**
- [How to Calculate Outliers](https://www.dataversity.net/how-to-calculate-outliers/)
- [Removing Outliers Using Standard Deviation in Python](https://www.reneshbedre.com/blog/outlier-detection-py.html)
- [How to Use Statistics to Identify Outliers in Data](https://www.simplypsychology.org/outliers.html)

