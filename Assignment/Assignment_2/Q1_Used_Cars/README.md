# Used Car Price Analysis Project

## Project Overview
This project focuses on the comprehensive data cleaning, processing, and exploratory analysis of a large dataset of used cars. The primary goal is to transform the messy, raw data into a clean, feature-rich dataset ready for machine learning (e.g., price prediction). The project includes extensive data validation, missing value imputation, feature engineering, and a final analysis of brand-level statistics.

## Repository Structure

```
Q1_Used_Cars/
├── data_clean/                # Processed and cleand dataset
│   ├── clean_used_cars.csv    # The fully cleaned and encoded dataset                     
├── raw_data/
│   ├── metadata.txt
│   └── train.csv              # The original, unprocessed dataset
├── results/  
│   └── analysis_goal.csv  # The output of the final brand analysis
├── src/                       # Source code and notebooks
│   └── Assignment2_Used_Cars.ipynb     # R notebook for all cleaning and analysis
└── Assignment_2_Used_Cars_Report.docx  # Report amd finding documention
└── README.md                  # Project documentation
```

## Key Tasks Completed
- **Data Cleaning & Validation**: Standardized inconsistent units across Mileage, Engine, Power, and New_Price. Converted columns from text to numeric types and corrected an extreme outlier in Kilometers_Driven.

- **Missing Value Imputation**: Filled NAs using robust methods:

    - **Median**: Used for Mileage, Engine, and Power to avoid skew from outliers.

    - **Mode**: Used for Seats (the most common value, 5).

    - **Grouped Median**: Used a multi-step process for New_Price by first using the median for that car model, then a global median.

- **Feature Engineering**: Created new, valuable features:

    - **Car_Age**: Calculated from the Year column.

    - **Brand**: Extracted from the Name column.

    - **Kilometers_Per_Year**: Normalized metric for car usage.

    - **Is_First_Owner**: A binary (0/1) version of the Owner_Type column.

- **One-Hot Encoding**: Transformed categorical columns (Fuel_Type, Transmission, Brand, Location) into a numeric format suitable for modeling.

- **Brand-Level Analysis**: Used dplyr verbs to group first-owner cars by brand and analyze the average price, power, and annual usage.

## Datasets Description
- **File**: [/raw_data/train.csv](https://github.com/mosomo82/COMP_SCI_5530/blob/main/Assignment/Assignment_2/Q1_Used_Cars/raw_data/train.csv)
- **Description**: [/raw_data/metadata.txt](https://github.com/mosomo82/COMP_SCI_5530/blob/main/Assignment/Assignment_2/Q1_Used_Cars/raw_data/metadata.txt)

## Key Findings & Analysis
The final analysis, saved in [/results/analysis_goal.csv](https://github.com/mosomo82/COMP_SCI_5530/blob/main/Assignment/Assignment_2/Q1_Used_Cars/results/analysis_goal.csv), focused on first-owner cars to compare popular brands.

- **Most Expensive (Popular Brands)**:

    1. Mercedes-Benz: 29.06 Lakh

    2. BMW: 27.56 Lakh

    3. Audi: 26.21 Lakh

- **Highest Average Annual Usage (Popular Brands)**:

    1. Toyota: 6,117 km/year

    2. Mahindra: 5,404 km/year

    3. Skoda: 5,109 km/year

- **Least Driven (Popular Brands)**:

    1. Hyundai: 3,973 km/year

    2. Honda: 4,078 km/year

    3. Maruti: 4,212 km/year

# Notes
- The `New_Price` column had over 86% missing data. While it was imputed using a robust grouped-median strategy, an alternative approach would be to drop this column entirely to prevent model bias.

## Installation / Setup

- **Requirement (R Libraries)**: The notebook relies on several R packages for data manipulation and analysis. You can install them by running:
```R
install.packages(c("dplyr", "tidyr", "readr", "stringr", "ggplot2")
```

- **Enviroment**: This assignement was built using **R** and is intended to be run in an environment like Google Colab or RStudio.
    * **Google Colab Setup:** To run in Colab, open `src/Assignment2_Used_Cars.ipynb`, then select **Runtime > Change runtime type > Select R > Save**.

## How to Run the Project

**1.** Open the notebooks in [src/*.ipynb](https://github.com/mosomo82/COMP_SCI_5530/blob/main/Assignment/Assignment_2/Q1_Used_Cars/src/Assignment2_Used_Cars.ipynb) (e.g. in Google Colab) to explore data and processess.

**2.** Run top-to-bottom. Output will be saved locally to see the analysis and findings. 

## Future Work/Next Steps:

- **Build Prediction Model**: The `clean_used_cars.csv` dataset is perfectly prepared for machine learning. The clear next step is to build regression models (e.g., Linear Regression, Random Forest) to predict the selling price `New_Price`
- **Evaluate Performace**: Measure your models' accuracy using metrics like Root Mean Squared Error ($\sqrt{RMSE}$) and R-squared ($R^2$) to see how closely your predictions match the actual selling prices.

## License

This project is licensed under the UMKC License. 

## Authors/Contributors:

- **Tony Nguyen** - [Github Profile](https://github.com/mosomo82)

## Acknowledgements

- Special thanks to Professor. Shah  for guidance on the project.
