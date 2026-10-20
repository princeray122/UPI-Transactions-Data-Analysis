# 💳 UPI Transactions Data Analysis | Power BI

### 📊 Dashboard Link

[**View Interactive Power BI Dashboard**](https://app.powerbi.com/links/1HMDusVnpT?ctid=61363c43-8420-43ca-8f82-801627e16cdf\&pbi_source=linkShare\&bookmarkGuid=e727a4a8-ec1c-45b1-be4c-c9cb88cf1ad3)

---

## 📌 Problem Statement

This project focuses on analyzing UPI transaction data using Microsoft Power BI to explore transaction patterns, monthly trends, customer demographics, and transaction balances.

The dashboard enables users to analyze transaction data across different banks, cities, device types, genders, age groups, merchants, payment methods, transaction purposes, and transaction types.

Interactive slicers allow users to filter transaction records based on specific attributes. Synced slicers maintain consistent selections across report pages, while report-level filters help control the data displayed throughout the report.

The project also incorporates bookmarks to switch between different report views, including transaction-related analysis, remaining balance analysis, and monthly line and column charts.

The main objective is to transform transaction data into an interactive report that makes it easier to explore patterns across customers, banks, payment categories, and time periods.

## 🎯 Project Objectives

- Analyze monthly trends in transaction amounts and balances.
- Categorize customers into age groups using DAX.
- Explore transactions by sending and receiving banks.
- Analyze transaction patterns across cities and device types.
- Examine transactions by gender, merchant, payment method, purpose, and transaction type.
- Compare monthly trends using line charts and column charts.
- Configure synced slicers for consistent filtering across report pages.
- Apply report-level filters for report-wide analysis.
- Create bookmarks for transaction and remaining balance views.
- Build an interactive and user-friendly Power BI report.

## 🛠️ Tools & Technologies Used

- **Microsoft Power BI Desktop** – Dashboard development and visualization
- **Power Query** – Data cleaning and transformation
- **DAX** – Calculated columns and measures
- **Data Modeling** – Organizing data for analysis
- **Power BI Service** – Publishing and sharing the report
- **Bookmarks** – Interactive report navigation
- **Synced Slicers** – Consistent filtering across report pages

## 🧹 Steps Followed

- **Step 1:** Loaded the UPI transaction dataset into Power BI Desktop.

- **Step 2:** Opened Power Query Editor to inspect the dataset and understand its structure.

- **Step 3:** Used data profiling features to examine column quality, distribution, and potential data quality issues.

- **Step 4:** Cleaned and transformed the data using Power Query as required.

- **Step 5:** Reviewed transaction fields such as BankNameSent, BankNameReceived, City, DeviceType, Gender, CustomerAge, MerchantName, PaymentMethod, Purpose, and TransactionType.

- **Step 6:** Created an Age Group calculated column using DAX to classify customers into three categories: A1, A2, and A3.

- **Step 7:** Prepared transaction and date fields for monthly trend analysis.

- **Step 8:** Added slicers for Bank Name Sent, Bank Name Received, City, Device Type, Gender, Age Group, Merchant Name, Payment Method, Purpose, and Transaction Type.

- **Step 9:** Configured synced slicers to maintain consistent selections across report pages where required.

- **Step 10:** Applied report-level filters to control the data displayed throughout the report.

- **Step 11:** Created monthly line charts to analyze changes in transaction amounts and balances.

- **Step 12:** Added column chart alternatives to compare monthly values using a different visualization.

- **Step 13:** Created bookmark buttons to switch between Line Chart Amounts, Column Chart Amounts, Line Chart Balance, and Column Chart Balance.

- **Step 14:** Added a matrix visual and a second report page to support additional analysis.

- **Step 15:** Configured bookmarks for transaction-related views and remaining balance analysis.

- **Step 16:** Formatted visuals, slicers, chart titles, labels, and buttons to improve report readability and navigation.

- **Step 17:** Published the report to Power BI Service and generated a shareable dashboard link.

*Note: These steps describe the reported project workflow. Keep the steps that accurately reflect your completed Power BI file.*

## 🧮 DAX Calculations

### 1. Age Group Classification

A calculated column was created using DAX to categorize customers based on the `CustomerAge` field.

```dax
Age Group =
IF(
    'UPI Transactions'[CustomerAge] <= 25,
    "A1",
    IF(
        'UPI Transactions'[CustomerAge] <= 35,
        "A2",
        "A3"
    )
)
```

**Classification Logic:**

| Customer Age          | Age Group |
| --------------------- | --------- |
| 25 or below           | A1        |
| Above 25 and up to 35 | A2        |
| Above 35              | A3        |

This calculated column allows users to filter transaction records by age group and explore demographic patterns.

*Note: The formula assumes `CustomerAge` contains valid numeric age values. Blank or invalid age values may require separate handling.*

### 2. Additional Measures

Other measures can be added according to the fields available in the dataset. The following are examples, not confirmed measures from the current report.

**Total Transactions**

```dax
Total Transactions =
COUNTROWS('UPI Transactions')
```

**Total Transaction Amount**

```dax
Total Transaction Amount =
SUM('UPI Transactions'[Amount])
```

**Total Remaining Balance**

```dax
Total Remaining Balance =
SUM('UPI Transactions'[Remaining Balance])
```

*Important: Use these additional measures only if the corresponding columns exist in your model. Replace the table and column names if necessary.*

## 📈 Dashboard Features

### 1. Age Group Analysis

- Categorizes customers into A1, A2, and A3 using the `CustomerAge` field.
- Provides an age-based slicer for filtering transactions.
- Supports demographic analysis across customer age categories.

### 2. Interactive Slicers

The report includes slicers for:

- Bank Name Sent
- Bank Name Received
- City
- Device Type
- Gender
- Age Group
- Merchant Name
- Payment Method
- Purpose
- Transaction Type

These slicers allow users to explore transaction records based on selected categories.

### 3. Monthly Transaction Analysis

- Displays monthly trends for transaction amounts.
- Supports line chart and column chart views.
- Makes it easier to compare changes in monthly transaction values.

### 4. Remaining Balance Analysis

- Displays monthly balance trends.
- Allows comparison using line and column charts.
- Supports analysis of balance patterns across the selected period.

### 5. Synced Slicers

- Maintains consistent filter selections across report pages where synchronization is enabled.
- Improves navigation between different analytical views.
- Reduces the need to reapply filters manually.

### 6. Report-Level Filters

- Applies filters across the report.
- Helps users focus on the required transaction data.
- Supports consistent filtering across report pages.

### 7. Bookmarks and Interactive Navigation

Bookmarks are used to switch between different report views, including:

- Line Chart Amounts
- Column Chart Amounts
- Line Chart Balance
- Column Chart Balance
- Transaction-related views
- Remaining balance views

This functionality improves report navigation and allows users to switch between prepared visual layouts.

### 8. Matrix Visual

The matrix visual provides an additional way to organize and examine transaction information across relevant categories and measures.

### 9. Multiple Report Pages

The report contains multiple pages to organize the analysis into different views and make the dashboard easier to navigate.

## 🖼️ Dashboard Preview

### Main Dashboard
The dashboard includes transaction-related slicers and monthly balance analysis, along with buttons for switching between different chart views.

<img width="602" height="338" alt="Image" src="https://github.com/user-attachments/assets/a9149d11-aacd-4d78-a231-5225d6a77a89" />


### Transaction Analysis

<img width="603" height="340" alt="Image" src="https://github.com/user-attachments/assets/7b682ffc-a497-4814-8598-5569b4843155" />

### Remaining Balance Analysis

<img width="597" height="337" alt="Image" src="https://github.com/user-attachments/assets/484f0ff3-c946-495c-b623-a3a5026f698b" />
```



## 💡 Key Insights and Analysis

The dashboard can be used to investigate the following questions:

1. **Monthly Trends:** How do transaction amounts and balances change across months?

2. **Age Group Analysis:** How do transaction patterns differ among A1, A2, and A3 customers?

3. **Bank Analysis:** How do transactions vary by sending and receiving banks?

4. **Geographical Analysis:** How do transaction records differ across cities?

5. **Device Analysis:** How do transaction patterns vary by device type?

6. **Payment Method Analysis:** How do transaction records differ across payment methods?

7. **Merchant and Purpose Analysis:** How do transaction patterns vary by merchant, purpose, and transaction type?

8. **Interactive Reporting:** How do the displayed results change when users apply slicers, report-level filters, and bookmarks?

*Note: These are analysis opportunities based on the report's fields and functionality. Add numerical findings only after verifying them against the actual dataset and report.*

## 💼 Business Recommendations

- Use monthly trends to explore changes in transaction activity.
- Compare transaction patterns across age groups.
- Examine differences across banks, cities, and devices.
- Use payment method and merchant filters for focused analysis.
- Use bookmarks to make report navigation easier for stakeholders.
- Validate transaction metrics before making conclusions about customer behavior.

## 🚀 Skills Demonstrated

- Data Cleaning and Transformation
- Power Query
- DAX Calculated Columns
- Age Group Categorization
- Data Visualization
- Line and Column Charts
- Matrix Visuals
- Interactive Slicer Configuration
- Synced Slicers
- Report-Level Filters
- Bookmarks and Report Navigation
- Power BI Service Publishing
- Interactive Dashboard Development

## 📁 Repository Structure

```text
UPI-Transactions-Data-Analysis/
│
├── README.md
├── images/
│   ├── upi-dashboard.png
│   ├── transaction-analysis.png
│   └── balance-analysis.png
├── dataset/
│   └── upi-transactions.csv
└── UPI-Transactions-Analysis.pbix
```

Upload the dashboard screenshots and project files using these filenames, or update the paths to match your actual repository. Share the dataset and Power BI file only if you have permission to do so.

## 📝 Conclusion

The UPI Transactions Data Analysis project demonstrates how Power BI can be used to explore transaction data through data cleaning, age group categorization, interactive slicers, synced filters, report-level filters, matrix visuals, monthly charts, and bookmarks.

By combining data preparation and interactive reporting features, the project provides a flexible way to analyze transaction patterns across customer demographics, banks, merchants, devices, payment methods, and time periods.

## 👨‍💻 Author

**Project:** UPI Transactions Data Analysis
**Tool:** Microsoft Power BI
**Focus:** Data Analytics, Transaction Analysis, and Interactive Reporting
