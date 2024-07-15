# Call Center Trends

## Problem Statement

Welcome to the Call Center Trends Analysis project! This repository contains Power BI dashboards and analysis aimed at enhancing the efficiency and customer satisfaction of call centers. Through detailed metrics and interactive visualizations, we provide insights into call volumes, agent performance, customer satisfaction, and more.


### Steps followed 

### Step 1: Load Data
- Loaded the dataset into Power BI Desktop from a CSV file.

### Step 2: Data Profiling
- Opened Power Query Editor.
- Enabled "Column Distribution," "Column Quality," and "Column Profile" options for comprehensive data profiling.
- Selected "Column profiling based on entire dataset" for accurate analysis.

### Step 3: Data Cleaning
- Observed no errors or empty values except in the "Arrival Delay" column.
- Excluded null values from average delay calculations as they were less than 1%.

### Step 4: Dashboard Design
- Selected a theme under the View tab for a consistent visual style.

### Step 5: Dynamic Visualizations
- Created dynamic visualizations to analyze call center performance:
  - **Donut Charts**: Visualizing answered and resolved calls categorized by Yes/No.
  - **Gauge**: Displaying average customer satisfaction level.
  - **Column Chart**: Showing the number of calls per month.
  - **Matrix View**: Summarizing agent statistics.
  - **Card**: Displaying the average speed of answer.
  - **Slicers**: For agent names, topics, and dates to filter data dynamically.

### Step 6: DAX Calculations
- Created calculated columns and measures using DAX:
  - **Number of Answered Calls**:
    ```dax
    # of Answered = CALCULATE(DISTINCTCOUNT('Call Center'[Call Id]), FILTER('Call Center', 'Call Center'[Answered (Y/N)] = "Y"))
    ```
  - **Number of Resolved Calls**:
    ```dax
    # of Resolved = CALCULATE(DISTINCTCOUNT('Call Center'[Call Id]), FILTER('Call Center', 'Call Center'[Resolved] = "Y"))
    ```
  - **Target Value Satisfaction**:
    ```dax
    Target Value Satisfaction = 4.5
    ```

### Step 7: Publish to Power BI Service
- Published the report to Power BI Service for sharing and collaboration.



# Snapshot of Dashboard (Power BI Service)

![Published Page](https://github.com/user-attachments/assets/a13cf7ee-d58f-4726-9b4e-f792c6d65cf5)

 
 # Report Snapshot (Power BI DESKTOP)

 
![Call Center Trends Dashboard](https://github.com/user-attachments/assets/2c128f31-c0e0-4b70-90f2-4aedb38eb425)

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
