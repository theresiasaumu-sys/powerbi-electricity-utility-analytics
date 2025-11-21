# 📊 Electricity Utility Power BI Capstone Project

*A comprehensive analytics project featuring data modeling, DAX, enterprise BI capabilities, and a full analytical case study.*

## 📁 Repository Contents

This repository contains:

* **Electricity_Utility_Analytics.pbix** – Main Power BI project file
* **/screenshots** – Visual screenshots of dashboards and report pages *(add yours after uploading)*
* **Project Question Set (Basic → Highly Technical)**
* **Project Write-up for Research Questions**
* **LinkedIn write-up included for context**

---

# 🚀 Project Overview

This capstone Power BI project analyzes electricity consumption, billing, and revenue recovery across 5,000+ customers for a fictional utility company.
The primary analytical challenge was to validate management’s claim that **postpaid customers in the South region were responsible for poor revenue recovery**.

The report includes:

* 8 interconnected dashboard pages
* 15+ custom DAX measures
* Data modeling with relationships, hierarchies, and composite models
* Advanced analytics (rolling averages, YTD, drill-through, what-if simulation)
* Enterprise-grade features including RLS, incremental refresh & PowerApps integration

---

# 🧱 Data Architecture & Modeling

The solution integrates multiple datasets:

| Dataset                         | Description                                       |
| ------------------------------- | ------------------------------------------------- |
| **Electricity_Consumption.csv** | kWh usage by customer, month, meter type, region  |
| **Revenue_Billing.csv**         | Amount billed, amount paid, outstanding revenue   |
| **Customer_Metadata.csv**       | Customer type, location, meter type, tariff class |

A star-schema relational model was built using **CustomerID** and **Month** as core keys.

---

# 📘 Full Project Question Set

### **SECTION A – Basic (Fundamentals & Data Handling)**

1. What is Power BI and how does it differ from Excel?
2. Steps to load CSV into Power BI
3. Difference between Power Query Editor and Data View
4. From Electricity_Consumption.csv:

   * (a) Total rows/columns
   * (b) Three data types converted
5. Purpose of relationships
6. Bar chart: Total Consumption by CustomerType
7. Card: Total Customers
8. Slicer: MeterType
9. Filters: visual-level vs page-level
10. Define DAX + simple example

### **SECTION B – Intermediate (Data Modeling & DAX Logic)**

11. Create relationship using CustomerID + Month
12. DAX: Outstanding Revenue
13. DAX: Recovery Rate %
14. Line Chart: Revenue Billed vs Paid by Month
15. Highest average consumption by CustomerType
16. Donut: Payment Status distribution
17. Tree Map: Revenue Billed by Customer Type
18. Tooltip showing Recovery Rate
19. Difference between Calculated Column & Measure
20. Handling missing values in Power Query

### **SECTION C – Advanced (Performance, Modelling, Storytelling)**

21. What-If parameter: ±10% Tariff Rate
22. Drill-through page for customer
23. DAX: Monthly Growth (Revenue Paid)
24. Top 10 Customers by Consumption
25. Visual: Recovery Rate by MeterType + interpretation
26. Conditional formatting for Recovery Rate < 0.7
27. Large dataset optimization strategies
28. Hierarchy: Region → CustomerType → CustomerID
29. YTD Revenue Paid
30. KPI: Current vs Previous Month Recovery Rate

### **SECTION D – Highly Technical (Enterprise Analytics & Automation)**

31. Implement incremental refresh
32. Configure Power BI Gateway
33. PowerApps visual for flagging unpaid bills
34. Q&A visual sample queries
35. Row-Level Security (RLS) rule
36. DAX: Rolling 3-Month Average Recovery Rate
37. Bookmark navigator (Consumption vs Revenue view)
38. Publish & share with limited access
39. Composite model with external dataset (weather, population, etc.)
40. Automated ingestion flow via Power Automate or Azure Data Factory

---

# 🎯 Capstone Analytical Challenge (Management Claim)

### **Claim:**

“Postpaid customers are responsible for poor revenue recovery in the South region.”

### **Findings:**

The data disproved the hypothesis:

* **Postpaid recovery rate:** **81.95%**
* **Prepaid recovery rate:** **82.00%**
* **Key driver:** Prepaid customers accounted for **₦1.04M (65.44%)** of total outstanding revenue.
* **Regional patterns** showed no statistically meaningful underperformance by postpaid customers in the South.

### **Supporting Visuals:**

<img width="1919" height="911" alt="Screenshot 2025-11-21 090726" src="https://github.com/user-attachments/assets/3c4bdd11-aeeb-44c9-a914-d71b81921c58" />

* Recovery Rate for Postpaid Customers in South Region
* Recovery Rate for Prepaid Customers in South Region
* Outstanding Revenue by Meter Type (Prepaid/Postpaid)
* Overall Recovery Rate 

### **DAX Measures (examples):**

```DAX
Recovery Rate for Prepaid = CALCULATE([Recovery Rate (%)],Electricity_Consumption[Meter Type]="Prepaid",'Electricity_Consumption'[Region]="South")
```

```DAX
Recovery Rate for Postpaid = CALCULATE([Recovery Rate (%)],Electricity_Consumption[Meter Type]="Postpaid",'Electricity_Consumption'[Region]="South")
```

### **Recommendation:**

Implement an automated follow-up system targeted at **prepaid customers**, since they generate the majority of outstanding revenue. Integrate SMS reminders, auto-blocking rules for persistent debtors, and tariff insights from the What-If parameter to guide price adjustments. This provides a more accurate intervention than focusing on postpaid customers, who are not the root cause of low recovery.

---

# 🖼️ Screenshots
(TODO UPDATE)

```
/screenshots
  ├── dashboard_overview.png
  ├── revenue_recovery_page.png
  ├── drillthrough_customer_view.png
  ├── what_if_parameter_simulation.png
```

---

# ▶️ How to Use This Repository

### **1. Clone the repository**

```bash
git clone https://github.com/yourusername/electricity-utility-powerbi-capstone.git
```

### **2. Open the PBIX file**

You need **Power BI Desktop (latest version)**.

---

# 🔗 LinkedIn Project Write-Up

My full write-up has been included in the repository (see `/LinkedIn_Writeup.txt`).
It summarizes:

* Project challenge
* Enterprise BI features
* Technical modeling
* Key analytical insights
* Business recommendations

---

# 📜 License

MIT License

---
