# Consumer Complaints Analysis — Power Query + Power BI Project

This project demonstrates a Power BI dashboard and Power Query workflow applied to a real-world consumer complaints dataset from Kaggle. The goal was to clean, transform, and visualize complaint data for insights relevant to AML/KYC and customer service analysis.

## 📁 Project Structure

This project uses the Consumer Complaints dataset by Anand Shaw on Kaggle. It contains ~14,000 complaints related to banking and financial products submitted by customers in the U.S.

### Key Fields:
- Date received, Date resolved
- Company, Company Type
- Product, Issue
- State, Submitted via
- Timely response?, Consumer disputed?
- Complaint narrative, Complaint ID
- Plus engineered fields like: Product - Issue, Resolution Time (Hours), Year, Month, Complaint Response Category

## ✅ Transformation Steps

**Part A – Power Query Core Steps**
- Removed null rows and duplicate columns
- Split “Company” into Company Name and Company Type
- Merged Product + Issue into a new column
- Added custom index starting from 1001
- Created conditional column based on resolution speed
- Calculated resolution time in hours
- Performed column trimming, case formatting, and prefix/suffix additions
- Used extract tools to isolate Month and Day
- Duplicated key columns for testing
- Sorted by Year and Resolution Time (in days)

**Part B – Smart Additions**
- Removed redundant columns like Date resolved.1
- Trimmed and replaced nulls in Company Type with “NA”
- Grouped by Company Name to count complaints (separate query)
- Exported key visuals to CSV for external use
- Added pie charts for Timely Response and Customer Dispute analysis
- Created a clustered column chart with slicer for companies with more than 50 complaints

## 📈 Visuals Included (Power BI)  

All visuals were built with **No DAX used** and exported to CSV.  
- Clustered Bar Chart: Complaints by Product  
- Line Chart: Complaint trend by Date received (Month-Year)  
- Donut Chart: Submission method (Submitted via)  
- Treemap: Complaint volume by State  
- Map: State-wise complaints colored by Company Type  
- Table: Complaint ID, Issue, Dates, and resolution info  
- Matrix: Product vs State complaint count  
- Pie Charts: Timely response and Dispute status  
- Clustered Column Chart with slicer: Companies with more than 50 complaints  

## 🧰 Tools & Techniques Used  
- Power BI Desktop  
- Power Query  
- Column splitting, trimming, replacing, custom columns  
- Conditional logic, extract by delimiter  
- Visual filtering and interaction setup  
- Export to CSV from visuals

## 📚 Dataset Source  
Kaggle - Consumer Complaints Dataset by Anand Shaw  
https://www.kaggle.com/datasets/anandshaw2001/consumer-complaints

## 📂 Key Files
- /data/raw/dataset_consumer_complaints.xlsx (original dataset)  
- /data/exports/ (CSV files of all visuals)  
- /docs/power-query-instructions.pdf (step-by-step transformation summary)  
- /powerbi/consumer-complaints-powerbi-dashboard.pbix (Power BI file)

## 📌 Use Case  
This project simulates how a compliance or support analyst might explore customer complaints for resolution efficiency, regional trends, and dispute resolution — all through clean Power Query-based transformations and simple Power BI visuals.
