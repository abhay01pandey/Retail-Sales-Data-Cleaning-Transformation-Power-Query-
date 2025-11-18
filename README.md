# Retail-Sales-Data-Cleaning-Transformation-Power-Query
This project focuses on cleaning, transforming, and integrating a multi-file retail sales dataset using Excel Power Query.   The goal was to prepare a fully structured and analysis-ready dataset by fixing quality issues, standardizing fields, and engineering new metrics.

## Dataset Overview
The project uses multiple CSV files stored in a local directory:
- Customers.csv  
- Products.csv  
- Regions.csv  
- Stores.csv  
- Returns_1997-1998.csv  
- Transactions_1997.csv  
- Transactions_1998.csv  

Each file was imported as a separate Power Query table and cleaned individually.

---

## Tools Used
- *Microsoft Excel*
- *Power Query*

---

## Data Cleaning & Transformation Steps

### *1. Customers Table*
- Trimmed and cleaned text fields  
- Fixed inconsistent data types  
- Standardized missing values  
- Calculated *Age*  
- Calculated *Membership Duration*  
- Created *member_card_num* (classification using conditional column)

---

### *2. Products Table*
- Standardized product attributes  
- Replaced inconsistent text values  
- Cleaned product categories and data types

---

### *3. Regions Table*
- Cleaned region IDs  
- Standardized district & region names  
- Ensured proper data types for merge compatibility

---

### *4. Stores Table*
- Cleaned store details  
- Removed unnecessary columns (street address)  
- Standardized store identifiers

---

### *5. Returns Table*
- Sorted return records  
- Merged with Products to pull product details  
- Calculated *Return_amount = quantity × retail_price*

---

### *6. Transactions (1997 & 1998)*
- Cleaned both datasets  
- Standardized date formats using locale-based type conversion  
- *Appended 1997 + 1998* into one unified table  
- Merged with Products to enrich transaction details  
- Calculated:
  - *Sales = quantity × product_retail_price*
  - *Cost_price = quantity × product_cost*
  - *Profit_margin = Sales – Cost_price*

---

## Final Output
The final cleaned dataset includes:
- Standardized customer profile table  
- Consistent product master table  
- Integrated region & store information  
- Clean return records with calculated return value  
- Combined transaction table (1997–1998) with:
  - Sales  
  - Cost_price  
  - Profit_margin  

---

## How to Reproduce
1. Place all CSV files into one folder  
2. Use *Get Data → From Folder* in Power Query  
3. Import each file as a separate query  
4. Apply the cleaning steps listed above  
5. Append the transaction tables  
6. Create calculated columns using *Add Column → Custom Column*  

