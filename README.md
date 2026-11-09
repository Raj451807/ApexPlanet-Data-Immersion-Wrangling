# ApexPlanet-Data-Immersion-Wrangling
Data Immersion and Wrangling internship project using Python, Pandas and NumPy. Includes data exploration, quality assessment, cleaning and transformation.


## 1. Project Overview

This project is part of my Data Analytics Internship at ApexPlanet Software Pvt. Ltd.

The main objective of this project is to understand, inspect, clean, and transform a raw dataset into an analysis-ready dataset using Python and its data analysis libraries.

The project focuses on data exploration, data quality assessment, data cleaning, and feature engineering.

## 2. Dataset Description

The project uses a sales transaction dataset containing **1,000 records and 12 original columns**.

The dataset includes information about:

- Order ID
- Order Date
- Customer ID
- Customer Name
- Age
- Gender
- City
- Product
- Category
- Quantity
- Unit Price
- Total Sales

This dataset helps understand customer purchasing patterns, product performance, and sales transactions.

## 3. Tools and Technologies Used

| Tool / Library | Purpose |
|---|---|
| Python | Programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Google Colab | Writing and executing Python code |
| GitHub | Project documentation and version control |

## 4. Data Quality Assessment

During the initial dataset inspection, the following issues were identified:

| Data Quality Issue | Finding |
|---|---:|
| Missing Age values | 20 |
| Missing City values | 13 |
| Exact duplicate rows | 0 |
| Records sharing a duplicate Order ID | 8 |
| Potential Total_Sales outliers | 19 |
| Invalid date values | 0 |
| Sales calculation mismatches | 0 |

**Note:** Repeated Order IDs were flagged for investigation rather than deleted because their transaction details were different. Potential sales outliers were also flagged rather than automatically removed.

## 5. Data Cleaning and Transformation

The following cleaning operations were performed:

1. Handled missing Age values using median imputation.
2. Handled missing City values by replacing them with "Unknown".
3. Converted Order_Date into a proper datetime format.
4. Standardized text columns by removing extra spaces and applying consistent title case.
5. Identified and flagged repeated Order IDs.
6. Checked numerical columns for potential outliers using the IQR method.
7. Verified Total_Sales using Quantity multiplied by Unit_Price.

## 6. Feature Engineering

New columns were created to make future analysis easier:

| New Column | Description |
|---|---|
| Order_Year | Year of the order |
| Order_Month | Numeric month of the order |
| Month_Name | Name of the order month |
| Quarter | Quarter of the year |
| Age_Group | Customer age category |
| Duplicate_Order_ID | Identifies repeated order IDs |
| Sales_Outlier | Flags potential sales outliers |

The final dataset contains 19 columns, including the original and engineered features.

## 7. Project Deliverables

The repository contains the following project files:

```text
ApexPlanet-Data-Immersion-Wrangling/
│
├── Dataset/
│   ├── ApexPlanet_DataAnalytics_Dataset.xlsx
│   ├── ApexPlanet_Cleaned_Dataset.csv
│   └── ApexPlanet_Cleaned_Dataset.xlsx
│
├── Reports/
│   ├── data_dictionary.csv
│   └── Data_Quality_Report.csv
│
├── Notebooks/
│   └── Data_Cleaning.ipynb
│
├── cleaning_script.py
│
└── README.md
```

## 8. Learning Outcomes

Through this project, I gained practical experience in:

- Understanding real-world datasets.
- Identifying data quality issues.
- Handling missing values and duplicate records.
- Performing data cleaning using Pandas.
- Detecting potential outliers using IQR.
- Creating new features from existing data.
- Preparing analysis-ready datasets.
- Documenting and managing projects using GitHub.

## 9. Conclusion

This project demonstrates the importance of data quality and preprocessing in the data analytics workflow.

By using Python, Pandas, and other data analysis libraries, the raw sales dataset was cleaned, transformed, and prepared for further exploratory data analysis and business insights.

---

**Project:** Data Immersion & Wrangling  
**Internship:** ApexPlanet Software Pvt. Ltd.  
**Tools:** Python | Pandas | NumPy | Matplotlib | Seaborn | Google Colab | GitHub
