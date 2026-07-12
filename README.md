# Sales & Customer Insights Dashboard (Power BI)

## 📊 Project Overview
An end-to-end interactive **Power BI Dashboard** built to deliver actionable insights into **Sales, Products, and Customer behavior**.  
The goal was to transform raw Excel data into a clean, structured model that supports data-driven decision-making.

---

## 🔍 Objectives
- Analyze sales performance and profitability across different regions, products, and customers.
- Identify churned customers and retention trends.
- Enable dynamic insights with parameters and filters.
- Improve report security and refresh performance using advanced Power BI features.

---

## 🧩 Data Source
Raw Excel files (`orders data.xlsx`, `info sec.xlsx`) containing:
- Sales transactions
- Product information
- Customer details
- Territory and currency data

---

## 🧹 Data Preparation (Power Query)
- Removed duplicates and blank rows  
- Handled null values and invalid records  
- Converted `DateKey` into valid date format  
- Cleaned strange values (e.g., `ProductKey = "SS"`)  
- Applied transformations for:
  - **GroupBy operations**  
  - **Filtering specific currencies or customers**

---

## 🧠 Data Modeling
- Built a **Star Schema** connecting:
  - `Fact_InternetSales` (Fact table)
  - `Dim_Customer`, `Dim_Product`, `Dim_SalesTerritory`, `Dim_Currency`, and `Calendar` (Dimension tables)
- Created a **Calendar table** for consistent date management
- Established relationships between all tables with proper cardinality

---

## 📈 Key Metrics (DAX)
- **Total Sales**
- **Total Cost**
- **Profit**
- **Profit Margin**
- **Churn Rate**
- **Active vs Churned Customers**

---

## ⚙️ Advanced Power BI Features
- **Parameters** → dynamic control for *Top N Products*  
- **Row-Level Security (RLS)** → ensures each user only sees their region’s data  
- **Incremental Refresh** → optimized data refresh performance for large datasets  
- **Custom Measures for UI Filters**
  ```DAX
  Year Filter = IF(ISFILTERED('Calendar'[Year]), SELECTEDVALUE('Calendar'[Year]), "")
  Currency Filter = IF(ISFILTERED('dim_Currency'[CurrencyName]), SELECTEDVALUE('dim_Currency'[CurrencyName]), "")
  ```

---

## 🖼️ Dashboard Highlights
- **Sales Trend by Month**
- **Top Products by Profit**
- **Sales by Country/Territory**
- **Customer Segmentation (Active vs Churned)**
- **Currency & Year Filter Cards (Dynamic Display)**

---

## 📂 Project Structure
```
📁 Sales & Customer Insights Dashboard (Power BI)
│
├── 📊 Sales_Insights_Final_Banque_Misr.pbix
├── 📄 orders data.xlsx
├── 📄 info sec.xlsx
├── 📁 images
│   ├── Overview.jpg
│   ├── Products.jpg
│   ├── RLS.jpg
│   ├── Currency Parameter.jpg
│   ├── Filtering Data.jpg
│   ├── Data Modeling.jpg
│   └── ...
└── README.md
```

---

## 🧩 Key Learnings
- Importance of clean data before visualization.
- How to integrate **RLS**, **Parameters**, and **Incremental Refresh** for real-world reporting.
- Designing dashboards that balance **performance**, **clarity**, and **interactivity**.

---

## 🚀 Outcome
A fully interactive, secure, and dynamic Power BI dashboard that:
- Summarizes thousands of sales records in seconds
- Enables decision-makers to explore and act on insights instantly
- Demonstrates the full data analysis lifecycle — from cleaning to modeling to visualization

---

## 📷 Dashboard Preview
*(Include some screenshots here from your `/images` folder once uploaded)*

---

## 🧑‍💻 Tools Used
- Microsoft Power BI  
- Power Query  
- DAX  
- Excel

---

## 📚 Author
**Mohamed Heta**  
Data Analyst | Power BI Developer  
#MAKE_DATA_TALK  
#معلومة_في_السكة
