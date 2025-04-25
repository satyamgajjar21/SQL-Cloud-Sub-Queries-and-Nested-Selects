# 🧠 SQL Hands-on Lab: Sub-Queries and Nested Selects

Welcome to the **Sub-Queries and Nested Selects Lab** using **MySQL**!  
This hands-on lab is part of the IBM Skills Network course and is designed to enhance your SQL querying skills through practical exercises using a sample **HR database**.

---

## 📌 Objectives

By completing this lab, you will be able to:

- ✅ Write SQL queries that demonstrate the necessity of using sub-queries
- ✅ Use sub-queries in the `WHERE` clause
- ✅ Use sub-queries in place of a **column expression**
- ✅ Use sub-queries in place of a **table expression**

---

## 🛠️ Tools Used

- **Database**: MySQL (via phpMyAdmin on SN Labs Cloud IDE)
- **Platform**: IBM Skills Network Labs (SN Labs)
- **Data Format**: CSV files
- **Tables**:  
  - `EMPLOYEES`  
  - `JOBS`  
  - `JOB_HISTORY`  
  - `DEPARTMENTS`  
  - `LOCATIONS`

---

## 🧩 Lab Setup Instructions

1. Launch **phpMyAdmin** via SN Toolbox (Cloud IDE).
2. Create a blank database named: `HR`
3. Run the provided `Script_Create_Tables.sql` to create the schema.
4. Upload the following `.csv` files via phpMyAdmin to populate tables:
   - `Employees.csv`
   - `Jobs.csv`
   - `JobsHistory.csv`
   - `Departments.csv`
   - `Locations.csv`

---

## 🧪 Practice Scenarios

### 🔍 1. Employees earning less than the average salary

```sql
SELECT * 
FROM EMPLOYEES 
WHERE SALARY < (SELECT AVG(SALARY) FROM EMPLOYEES);
