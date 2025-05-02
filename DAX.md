# 📊 DAX Measures for Financial Loan Report Analysis

This file contains all the DAX measures used in the **Financial Loan Analysis** Power BI report.

---

## 🔢 General Measures

1. Total Funded Amount

Total Funded Amount = 
SUM(
    financial_loan[Loan_Amount]
)
2. Total Amount Received

Total Amount Received = Total Amount Received = 
SUM(
    financial_loan[Total_Payment]
)

3. Average Interest Rate

Avg_Int_Rate = 
AVERAGE(
    financial_loan[Int_Rate]
)

4. Total Loan Application

Total Loan Application = COUNT(financial_loan[ID])

## Date & Time Intelligence

1. Date :-

Calendar_Table = CALENDAR(
    MIN(financial_loan[Issue_Date]),
    MAX(financial_loan[Issue_Date])
    )

2. Year :-

Year = FORMAT(Calendar_Table[Date], "yyyy")

3. Month 

Month = FORMAT(Calendar_Table[Date],"mmm")

4. Month Number 

Month_No = FORMAT(Calendar_Table[Date], "m")


🧪 Parameter Measures (for Dynamic Metric Selection)
I used a parameter slicer (from Modeling > New Parameter) 

This is the list the key measure switch:

Total Funded Amount
Total Amount Received
Total Loan Appplication
Average Interest Rate




