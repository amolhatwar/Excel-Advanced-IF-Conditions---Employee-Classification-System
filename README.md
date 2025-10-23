# Excel Advanced IF Conditions - Employee Classification System

## 🖼️ Screenshots
| Before Formatting | After Formatting | Final Output |
|:------------------:|:----------------:|:-------------:|
| ![Before][!Question_Image]

01. Question Img
<img src="https://github.com/amolhatwar/Excel-Advanced-IF-Conditions---Employee-Classification-System/blob/fc51db6738cffa22548e0c64d3e4bc410f444336/Question%20Screenshot.png" alt="image Description" Width="600">
<br>

01. Solution Img
<img src="https://github.com/amolhatwar/Excel-Advanced-IF-Conditions---Employee-Classification-System/blob/fc51db6738cffa22548e0c64d3e4bc410f444336/Solution%20Screenshot%2001.png" alt="image Description" Width="600">
<br>

02. Question Img
<img src="https://github.com/amolhatwar/Excel-Advanced-IF-Conditions---Employee-Classification-System/blob/fc51db6738cffa22548e0c64d3e4bc410f444336/Question%20Screenshot%2002.png" alt="image Description" Width="600">
<br>
02. Solution Img
<img src="https://github.com/amolhatwar/Excel-Advanced-IF-Conditions---Employee-Classification-System/blob/fc51db6738cffa22548e0c64d3e4bc410f444336/Solution%20Screenshot%2002.png" alt="image Description" Width="600">
<br>

03. Final Solution Img
<img src="https://github.com/amolhatwar/Excel-Advanced-IF-Conditions---Employee-Classification-System/blob/fc51db6738cffa22548e0c64d3e4bc410f444336/Solution%20Screenshot%20Final.png" alt="image Description" Width="600">
<br>

## Project Overview
This project demonstrates advanced Excel IF condition formulas to automate employee classification, performance evaluation, and promotion eligibility based on multiple criteria.

## What I Learned
Through this project, I mastered complex nested IF conditions in Excel to create dynamic employee management systems that automatically categorize and evaluate staff based on multiple business rules.

## Dataset Structure
The project uses an employee database with the following columns:
- **Department ID & Name**: Organizational structure
- **Annual Salary Budget (USD)**: Department budget allocation
- **Years with Company**: Employee tenure
- **Performance Score**: Rating scale (1-10)
- **Employee Type**: Senior/Junior classification
- **P.Status**: Performance status (Best/Good/Average/Poor)
- **Promotion**: Eligibility (Yes/No)

## Key Formulas Implemented

### 1. Employee Type Classification (Column F)
**Formula Used:**
```excel
=IF(D2>=3, "Senior", "Junior")
```
**Logic:** 
- Employees with 3+ years experience → Senior
- Less than 3 years → Junior

**Insight:** Automatically classifies 28 departments based on tenure, creating clear seniority levels.

---

### 2. Performance Status Evaluation (Column G)
**Formula Used:**
```excel
=IF(E2>=8, "Best", IF(E2>=6, "Good", IF(E2>=4, "Average", "Poor")))
```
**Logic:**
- Performance Score ≥ 8 → Best
- Performance Score ≥ 6 → Good
- Performance Score ≥ 4 → Average
- Performance Score < 4 → Poor

**Insight:** Creates 4-tier performance classification system. From the data:
- **Best performers**: Financial Planning (10), Corporate Affairs (10), Budgeting (9)
- **Poor performers**: Executive Management (2), Human Resources (2), Recruitment (2)

---

### 3. Promotion Eligibility (Column H)
**Formula Used:**
```excel
=IF(AND(E2>=5, D2>=4), "Yes", "No")
```
**Logic:**
- Performance Score ≥ 5 AND Years with Company ≥ 4 → Eligible for promotion
- Otherwise → Not eligible

**Complex Conditions:**
- Requires BOTH criteria to be met simultaneously
- Uses AND function within IF statement

**Insight:** Out of 28 departments analyzed:
- **Eligible for promotion**: 18 departments (64%)
- **Not eligible**: 10 departments (36%)

Notable promotion-ready departments:
- Financial Planning and Analysis (10 score, 16 years)
- Compensation and Benefits (9 score, 20 years)
- Cost Accounting (9 score, 14 years)

---

## Advanced Formula Techniques Used

### Nested IF Statements
Created multi-level conditional logic to handle 4 different performance tiers:
```excel
IF(condition1, result1, IF(condition2, result2, IF(condition3, result3, result4)))
```

### Logical Functions
- **AND()**: Combined multiple conditions for promotion eligibility
- **Comparison operators**: >=, >, <, = for threshold evaluation

### Formula Combinations
Integrated multiple IF conditions across columns to create interconnected classification systems.

---

## Business Insights from the Data

### Performance Distribution
- **Best (≥8)**: 7 departments
- **Good (6-7)**: 5 departments  
- **Average (4-5)**: 9 departments
- **Poor (<4)**: 7 departments

### Seniority Analysis
- **All employees classified as Senior** (all have 3+ years experience)
- Longest tenure: Executive Management (21 years)
- Shortest tenure: Corporate Strategy (1 year), Taxation (1 year)

### High-Budget Departments
- Finance: $1,500,000
- Operations: $1,300,000
- Executive Management: $2,500,000
- Legal: $1,000,000

### Promotion-Ready High Performers
Departments with both high performance AND promotion eligibility:
- Financial Planning and Analysis (Score: 10)
- Budgeting (Score: 9)
- Compensation and Benefits (Score: 9)
- Cost Accounting (Score: 9)

---

## Skills Demonstrated

✅ **Nested IF Conditions**: Multi-level decision trees  
✅ **Logical Operators**: AND, OR conditions  
✅ **Threshold-based Classification**: Performance tiers  
✅ **Business Rule Implementation**: Promotion eligibility logic  
✅ **Data Analysis**: Extracting insights from classification results  
✅ **Formula Debugging**: Testing edge cases and boundary conditions  

---

## Use Cases

This formula system can be applied to:
- Employee performance reviews
- Promotion eligibility screening
- Salary increment calculations
- Workforce planning and classification
- HR analytics dashboards
- Automated reporting systems

---

## How to Use

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/excel-if-conditions
```

2. **Open the Excel file**: Employee_Classification_System.xlsx

3. **Review the formulas** in columns F, G, and H

4. **Modify thresholds** based on your business requirements:
   - Change performance score thresholds
   - Adjust tenure requirements
   - Add additional classification criteria

---

## Sample Formula Breakdown

### Performance Status Formula
excel
=IF(E2>=8, "Best", IF(E2>=6, "Good", IF(E2>=4, "Average", "Poor")))
```

**How it works:**
1. First check: Is score ≥ 8? → Return "Best"
2. If not, check: Is score ≥ 6? → Return "Good"
3. If not, check: Is score ≥ 4? → Return "Average"
4. If none match → Return "Poor"

---

## Key Learnings

### 1. Nested IF Structure
Understanding the logic flow:
- Excel evaluates conditions from left to right
- First TRUE condition stops evaluation
- Important to order conditions from highest to lowest

### 2. AND Function in IF
Combining multiple criteria:
```excel
=IF(AND(condition1, condition2), "Yes", "No")
```
- ALL conditions must be TRUE
- Perfect for complex business rules

### 3. Practical Applications
- Automated employee classification
- Performance-based decision making
- Scalable to thousands of records
- Easy to audit and modify

---

## Future Enhancements

- [ ] Add SWITCH function for cleaner performance tiers
- [ ] Implement IFS function (Excel 2019+) for simplified nested logic
- [ ] Create dynamic thresholds using named ranges
- [ ] Add COUNTIF analysis for distribution statistics
- [ ] Build dashboard with conditional formatting

---

## Tool Used
Microsoft Excel
Functions: IF, Nested IF, AND
Data Analysis: Classification, Performance Evaluation

---

## Connect with Me
If you found this project helpful or want to discuss Excel automation:

🔗 [LinkedIn](https://www.linkedin.com/in/amolhatwar)  
🔗 [GitHub](https://github.com/amolhatwar)
🔗 [GitHub](https://amolhatwar.github.io)
