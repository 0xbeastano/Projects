# Customer Retention

## Problem Statement

Welcome to the Customer Retention Analysis project! This repository contains Power BI dashboards and analysis aimed at understanding and improving customer retention rates. Through detailed metrics and interactive visualizations, we provide insights into customer demographics, service usage, contract details, and more.


### Steps followed 

### Step 1: Load Data
- Loaded the dataset into Power BI Desktop from a CSV file.

### Step 2: Data Profiling
- Opened Power Query Editor.
- Enabled "Column Distribution," "Column Quality," and "Column Profile" options for comprehensive data profiling.
- Selected "Column profiling based on entire dataset" for accurate analysis.

### Step 3: Data Cleaning
- Observed no errors or empty values except in the "Gender" column.
- Excluded null values from average delay calculations as they were less than 1%.

### Step 4: Dashboard Design
- Selected a theme under the View tab for a consistent visual style.

### Step 5: Dynamic Visualizations

#### Churn Dashboard
- Created visualizations to analyze churn factors:
  - **Donut Charts**: Gender distribution (Male/Female) and paperless billing (Yes/No).
  - **Bar Charts**: Analyzing subscription time, payment method, and types of contract.
  - **Multi Row Card**: Detailed view of phone services, streaming TV, streaming movies, device protection, tech support, and online security.
  - **Cards**: Displaying metrics such as customers at risk, percentage of tech tickets, percentage of admin tickets, yearly charges, and monthly charges.

#### Customer Risk Analysis Dashboard
- Designed visualizations to assess customer risk factors:
  - **Column Chart**: Churn rate by Internet Service provider.
  - **Clustered Line Chart**: Types of contract and years of contract analysis.
  - **Pie Charts**: Distribution of customers by internet services.
  - **Cards**: Total customers, churn rate percentage, yearly charges, sum of monthly charges.
  - **Slicers**: Filter options for risk of churn, internet services, and monthly subscription details.


### Step 6: DAX Calculations
- Created calculated columns and measures using DAX:
  - **Count of Churn for Yes**:
    ```dax
    Count of Churn for Yes = 
    CALCULATE ( COUNTA('churn'[Churn]), 'churn'[Churn] IN { "Yes" } )
    ```
  - **Dependents in %**:
    ```dax
    Dependents in % = DIVIDE (
    CALCULATE ( COUNT (churn[Dependents]),  
    churn[Dependents] = "Yes", churn  [Churn] = "Yes" ),
    CALCULATE ( COUNT (churn[Dependents]), churn[Churn] = "Yes" ),0)
    ```

### Step 7: Publish to Power BI Service
- Published the report to Power BI Service for sharing and collaboration.



# Snapshot of Dashboard (Power BI Service)

![Customer Retention Report](https://github.com/user-attachments/assets/9b7f15fb-4597-49ab-81d9-0fa2340639c6)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Customer Retention](https://github.com/user-attachments/assets/d4b5d378-9735-4cfb-ade5-91200657335a)

# Insights Generated

- **⏱️ Call Answering Efficiency**: Analyzed the speed of answer and its impact on customer satisfaction.
- **👩‍💼 Agent Performance**: Assessed individual agent performance based on resolution rates and customer satisfaction.
- **📞 Call Topics**: Identified trends in call topics to address common issues proactively.
- **⏳ Talk Duration**: Evaluated average talk duration to optimize call handling processes.
- **🚀 Actionable Recommendations**: Provided strategies to improve response times, enhance agent training, and increase overall customer satisfaction.

# Contact

If you have any questions or feedback, feel free to contact me at [pranit17patil@gmail.com](mailto:pranit17patil@gmail.com).

---

**Happy analyzing!** 😊
