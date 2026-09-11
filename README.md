# 📊 Maven Market — Transaction & Performance Analysis

## 📌 Project Overview

Maven Market — Transaction & Performance Analysis is an interactive **Power BI Business Intelligence project** developed to analyze transaction activity, product performance, profitability, returns, customer information, store locations, and regional activity.

The project transforms raw retail data into an interactive analytical report using **Power Query, data modeling, DAX, and data visualization**.

The dashboard is designed to provide a clear view of transaction performance and help identify important patterns across products, brands, stores, regions, customers, time periods, profitability, and returns.

---

## 🎯 Project Objective

The objective of this project was to build an interactive Power BI report that allows users to:

- Monitor transaction activity and performance
- Track current-month transactions
- Analyze product brand transaction volume
- Evaluate total profit and profit margin
- Monitor product returns and return rates
- Compare revenue against established targets
- Analyze weekly revenue trends
- Explore store and regional activity
- Examine customer-related information
- Identify meaningful business observations from the data

The project focuses on turning transactional data into a structured and interactive reporting solution rather than simply presenting raw numbers.

---

# 🗂️ Data Model

The Power BI model consists of seven tables representing different areas of the Maven Market dataset.

### Tables

| Table | Purpose |
|---|---|
| **Calendar** | Provides date-related information for time-based analysis |
| **Customers** | Contains customer information used for customer analysis and segmentation |
| **Products** | Contains product, brand, pricing, and cost information |
| **Regions** | Provides regional and geographic information |
| **Stores** | Contains store-level information and location attributes |
| **Return_Data** | Contains product return transaction information |
| **Transaction_Data** | Contains the primary transaction records used throughout the analysis |

The model connects transactional data with lookup tables to support consistent filtering and analysis across the report.

---

# 🔗 Data Modeling

The data model was designed using a dimensional approach.

Key relationships include:

- `Transaction_Data` → `Customers`
- `Transaction_Data` → `Products`
- `Transaction_Data` → `Stores`
- `Transaction_Data` → `Calendar`
- `Return_Data` → `Products`
- `Return_Data` → `Stores`
- `Return_Data` → `Calendar`
- `Stores` → `Regions`

The two transactional tables, `Transaction_Data` and `Return_Data`, are not directly connected to each other. Instead, shared lookup tables are used to support the analysis.

This structure helps maintain a clean and efficient analytical model.

---

# 🔄 Data Preparation & Transformation

Data preparation was completed using **Power Query**.

The main transformation activities included:

- Connecting to transaction data stored across multiple files
- Combining transaction data from multiple years
- Cleaning and standardizing the source data
- Promoting headers
- Correcting data types
- Handling null values
- Creating a discounted retail price
- Rounding pricing values to two decimal places
- Creating a full store address
- Extracting store area codes
- Creating calendar-related fields
- Preparing date fields for time-based analysis
- Organizing transaction and return data for Power BI modeling

These transformations helped create a consistent and analysis-ready dataset.

---

# 🧮 DAX & Analytical Calculations

DAX was used to create measures and calculated columns for the report.

## Key Measures

The report includes analytical measures such as:

- **Quantity Sold**
- **Quantity Returned**
- **Total Transactions**
- **Total Returns**
- **Return Rate**
- **% Weekend Transactions**
- **Total Revenue**
- **Total Cost**
- **Total Profit**
- **Profit Margin**
- **Revenue Target**
- **Current Month Transactions**
- **Current Month Profit**
- **Current Month Returns**
- **Last Month Revenue**
- **Last Month Profit**
- **Last Month Transactions**
- **YTD Revenue**
- **60-Day Revenue**

These measures allow the report to dynamically calculate performance based on the selected dates, products, stores, and other report filters.

---

## 📅 Calculated Columns

Additional calculated columns were created to support the analysis, including:

- **Weekend**
- **End of Month**
- **Current Age**
- **Priority**
- **Short Country**
- **House Number**

Calendar attributes were also prepared to support analysis by:

- Day
- Week
- Month
- Quarter
- Year

---

# 📊 Topline Performance Dashboard

The main **Topline Performance** page provides an executive-level summary of Maven Market transaction and performance information.

The page brings together:

- Current Month Transactions
- Current Month Profit
- Current Month Returns
- Product Brand performance
- Total Transactions
- Total Profit
- Profit Margin
- Return Rate
- Geographic analysis
- Weekly Revenue Trending
- Revenue vs. Target

![Maven Market Topline Performance](Screenshots/Screenshot_Maven_dashboard.jpg
Screenshots/Screenshot)

---

# 📌 Key Dashboard Metrics

## Current Month Transactions

The dashboard shows:

### **9,516 Current Month Transactions**

The current-month transaction figure is compared against a goal of approximately **10.09K**, providing an immediate indication of transaction performance against the target.

---

## Current Month Profit

The dashboard reports:

### **$36.91K Current Month Profit**

This is compared against a goal of approximately **$39.44K**, allowing users to quickly identify the current profit performance gap.

---

## Current Month Returns

The dashboard reports:

### **256 Current Month Returns**

The report indicates that current-month returns are above the established goal.

The Notes page identifies this as **4.48% above the goal of 245**.

This makes return activity an important metric to monitor alongside transaction and profitability performance.

---

# 🏆 Product Brand Analysis

The product brand matrix evaluates brands using multiple performance measures:

| Metric | Purpose |
|---|---|
| **Total Transactions** | Measures transaction volume by brand |
| **Total Profit** | Measures profit generated by each brand |
| **Profit Margin** | Evaluates profitability relative to revenue |
| **Return Rate** | Measures the rate of returned products |

The matrix uses **data bars and conditional formatting** to make differences between brands easier to identify.

A **Top 30** view is also used to focus the analysis on brands with the highest transaction volume.

### Leading Brand

**Hermanos** has the highest number of transactions among the displayed brands:

### **2,796 Transactions**

This makes Hermanos a leading brand based on transaction volume.

---

# 💰 Revenue & Target Analysis

The dashboard includes a **Revenue vs. Target** visualization to compare actual revenue performance against the established target.

The displayed values are approximately:

### **$61.91K Actual Revenue**

vs.

### **$69.36K Target**

This visualization allows users to quickly identify the gap between actual performance and the expected target.

---

# 📈 Weekly Revenue Trending

The **Weekly Revenue Trending** visual provides a time-based view of revenue activity throughout the year.

This analysis helps identify:

- Changes in weekly revenue
- Higher-performing periods
- Lower-performing periods
- Revenue fluctuations
- Potential seasonal patterns

Time-based analysis allows users to understand not only how much revenue was generated, but also how performance changed over time.

---

# 🌎 Geographic Analysis

The dashboard includes geographic analysis across:

- **USA**
- **Canada**
- **Mexico**

A map visualization is used to display store activity geographically.

This allows users to explore the distribution of stores and understand activity across different locations and countries.

---

# 📝 Notes & Insights Page

A dedicated **Notes** page was created to communicate important observations from the analysis and provide interactive navigation using Power BI bookmarks.

![Maven Market Notes](Screenshots/02_Notes.png)

The Notes page highlights several observations:

### 📍 Portland

Portland reaches **1,000 sales in December**.

### 🏆 Hermanos

Hermanos has the highest number of transactions with **2,796 transactions**.

### ⚠️ Current Month Returns

Current-month returns are **256**, which is **4.48% above the goal of 245**.

The Notes page demonstrates how Power BI can combine analytical findings with interactive navigation to improve the overall reporting experience.

---

# 📊 Overall Performance Reference

The analytical model produces the following overall metrics:

| KPI | Result |
|---|---:|
| **Quantity Sold** | 833,489 |
| **Quantity Returned** | 8,289 |
| **Total Transactions** | 269,720 |
| **Total Returns** | 7,087 |
| **Overall Return Rate** | 0.99% |

These values provide a high-level reference for the underlying transaction and return activity in the dataset.

---

# 🎛️ Power BI Features Used

The report incorporates a range of Power BI functionality, including:

- Interactive filters
- Bookmarks
- KPI cards
- Matrix visualizations
- Conditional formatting
- Data bars
- Gauge visualization
- Geographic maps
- Time-based trend analysis
- Top N filtering
- Dynamic DAX measures
- Target comparisons
- Interactive report navigation

These features allow users to move from high-level performance monitoring to more detailed analysis.

---

# 💡 Key Analytical Takeaways

The project demonstrates how transaction data can be analyzed from several different perspectives.

### Transaction Performance

Transaction volume can be monitored by month, product brand, store, and other dimensions to identify areas of strong or weak activity.

### Product Brand Performance

Brands can be compared using transaction volume, total profit, profit margin, and return rate rather than relying on a single performance measure.

### Profitability

Total profit and profit margin provide a deeper understanding of financial performance and help distinguish high-volume brands from highly profitable brands.

### Returns

Return quantities and return rates provide an additional perspective on product performance and help identify areas that may require further investigation.

### Revenue Performance

Actual revenue can be compared against targets to identify performance gaps.

### Geographic Performance

Store activity can be explored across the USA, Canada, and Mexico to understand geographic distribution.

### Time-Based Performance

Weekly and monthly analysis helps identify changes in performance over time.

---

# 🛠️ Tools & Technologies

### Business Intelligence
- Microsoft Power BI

### Data Transformation
- Power Query

### Analytical Calculations
- DAX

### Data Modeling
- Dimensional Data Modeling
- One-to-many relationships
- Lookup and transaction tables

### Data Visualization
- KPI Cards
- Matrix Visuals
- Conditional Formatting
- Data Bars
- Gauge Charts
- Geographic Maps
- Trend Analysis
- Interactive Filters
- Bookmarks

---

# 🧠 Skills Demonstrated

This project demonstrates practical skills in:

- Power BI
- Power Query
- DAX
- Data Cleaning
- Data Transformation
- Data Modeling
- Business Intelligence
- Data Visualization
- KPI Development
- Transaction Analysis
- Revenue Analysis
- Profitability Analysis
- Product Analysis
- Return Analysis
- Geographic Analysis
- Time-Series Analysis
- Business Storytelling
- Interactive Dashboard Development
- Analytical Problem Solving

---

# 🔍 End-to-End Analytical Workflow

The project follows an end-to-end data analytics workflow:

```text
Raw Data
    ↓
Data Cleaning
    ↓
Power Query Transformations
    ↓
Data Modeling
    ↓
DAX Calculations
    ↓
KPI Development
    ↓
Interactive Visualizations
    ↓
Performance Analysis
    ↓
Business Insights
