# 📊 Power BI Data Modeling Project

Welcome to my **Power BI Data Modeler** project!  
This project demonstrates professional-level skills in **data modeling**, **star schema design**, **hierarchies**, **relationship management**, and **matrix-based data validation**.  
It includes work done in **Power Query**, **Model View**, and **Report View**, following all instructions provided by my sir.

---

## ✨ Project Overview

This project focuses on designing a **clean, optimized, and fully functional data model** using:
- Two Fact Tables (`Sales_Fact`, `Returns_Fact`)
- Four Dimension Tables (`Customer_Dim`, `Product_Dim`, `Region_Dim`, `Date_Dim`)
- A **Star Schema** with proper cardinalities, directions, keys, hierarchies, and inactive relationships.

The final PBIX showcases:
- Transformed data  
- Validated relationships  
- Cleaned columns  
- Proper hierarchies  
- Three verification matrix tables  
- Professional model structure  
- Hidden surrogate keys  
- Meaningful data categories  

---

## 📁 Data Sources (Extracted Excel Files)

All datasets were provided as part of the PR.2 task and imported into Power BI via **Power Query**:

1. **Customer_Dim.xlsx**  
   - CustomerID (PK), FullName, Age, Gender, Segment

2. **Product_Dim.xlsx**  
   - ProductID (PK), ProductName, Category, Subcategory, Brand

3. **Region_Dim.xlsx**  
   - RegionID (PK), Country, State, City

4. **Date_Dim.xlsx**  
   - DateKey (PK), Date, Year, Quarter, Month, Fiscal Year

5. **Sales_Fact.xlsx**  
   - SalesID (PK), CustomerID, ProductID, RegionID, DateKey, Quantity, Revenue, Discount

6. **Returns_Fact.xlsx**  
   - ReturnID (PK), SalesID (FK), ReturnDateKey (FK), Reason

---

## 🧩 Data Model Features

### ✔️ **Star Schema Design**
- `Sales_Fact` as the central fact table  
- All dimension tables connected using **1:* relationships**
- `Returns_Fact` modeled as a **second fact table**  
- Inactive relationship created from `Returns_Fact[ReturnDateKey]` → `Date_Dim[DateKey]`

### ✔️ **Cardinality & Filter Directions**
- All relationships set to **Single direction**
- Fact tables on the *many* side  
- Dimension tables on the *one* side  
- One inactive relationship used for ReturnDateKey

---

## 🏗️ Model Enhancements

### 🔧 **Data Formatting**
Applied proper:
- Currency formats  
- Whole numbers  
- Date formats  

### 🔖 **Data Categories**
Defined for:
- Country → *Country*  
- State → *State*  
- City → *City*  
- Date → *Date*  
- ProductName → *Product*  

### 🗂️ **Hierarchies**
Three custom hierarchies were built:

#### 📅 **Date Hierarchy**
- Year → Quarter → Month → Date

#### 🌍 **Region Hierarchy**
- Country → State → City

#### 🛍️ **Product Hierarchy**
- Category → Subcategory → ProductName

### 👁️ **Hidden Columns**
All Primary Keys & Foreign Keys were hidden from report view:
- SalesID, ReturnID  
- CustomerID, ProductID, RegionID  
- DateKey, ReturnDateKey  

This keeps the report **clean and professional**.

---

## 📊 Verification Matrix Tables

As required, three matrix visuals were created:

### 1️⃣ **Sales grouped by Product Category & Region**
Includes:
- Category as rows  
- Country as sub-level  
- Sum of Revenue  

### 2️⃣ **Return Reasons by Fiscal Year**
- Fiscal Year as rows  
- Reasons as columns  
- Count of ReturnID  

### 3️⃣ **Revenue by Customer Segment**
- Segment as rows  
- Sum of Revenue as values  

These matrices helped validate data integrity, relationships, and hierarchies.

---

## 📝 Report View

<img src="ReportView.png" width="400" alt="Report View" />

**Verification matrices demonstrating sales breakdown, fiscal-year return analysis, and customer segment revenue validation.**

---

## 📝 Model View

<img src="ModelView.png" width="400" alt="Model View" />

**Complete Star Schema with dual fact tables, optimized relationships, and fully defined hierarchies.**

---

## 🗃️ Final Deliverables

The submitted folder contains:

- **✔️ Data Modeler.pbix** (final Power BI file)  
- **✔️ All 6 Excel source files**   
- **✔️ README.md (this file)**  

---

## 🚀 Conclusion

This project showcases:
- Strong understanding of **Power BI data modeling principles**
- Ability to work with **multiple fact tables**
- Clean & optimized relationship management  
- Hierarchical structuring  
- Verification through matrix visuals  
- Professional-level Power BI organization

If you'd like to explore or reuse this model, feel free to download the `.pbix` and plug in your own data! ✨

---

### 🔗 Created with dedication by Paree Sojitra 
