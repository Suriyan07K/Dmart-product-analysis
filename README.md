# DMart Product Catalogue — Data Analysis

## Project Overview

This project focuses on Exploratory Data Analysis (EDA) of a DMart product catalogue using Python. The objective is to understand product distribution, brand availability, category-wise pricing, and discount patterns through data cleaning, statistical summaries, and visualisations.

The project demonstrates practical Data Analyst skills, including data preprocessing, data quality checks, data exploration, visualisation, and business insight generation.

## Project Objectives

- Understand the structure and quality of the dataset.
- Handle missing values and perform data quality checks.
- Standardise quantity, category, and subcategory values.
- Analyse product listings by category, brand, subcategory, and quantity.
- Explore original prices, discounted prices, and discount percentages.
- Compare DMart Grocery rice listings with regular Grocery rice listings.
- Analyse men's and women's clothing categories and their discount patterns.
- Summarise findings and provide data-driven recommendations.

## Dataset Information

- **Dataset:** DMart.csv
- **Initial rows:** 5,189
- **Original columns:** 9
- **Working columns:** 10, including the derived `DiscountPercent` column.

### Columns Used

- `Name`
- `Brand`
- `Price`
- `DiscountedPrice`
- `Category`
- `SubCategory`
- `Quantity`
- `Description`
- `BreadCrumbs`
- `DiscountPercent`

> **Note:** This dataset represents product listings. It does not provide transaction-level sales or customer purchase history in the reviewed analysis. Therefore, the project focuses on catalogue-level insights rather than actual sales performance or customer behaviour.

## Technologies and Libraries

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly Express
- Google Colab / Jupyter Notebook

## Project Workflow

### 1. Data Understanding

- Loaded the dataset using pandas.
- Examined the number of rows and columns.
- Inspected data types and column names.
- Checked missing values and duplicate records.
- Generated descriptive statistics and unique-value summaries.

### 2. Data Cleaning

- Handled missing values in selected columns.
- Checked original and discounted prices for negative values and inconsistencies.
- Calculated the `DiscountPercent` feature.
- Standardised selected quantity units and text formats.
- Reviewed category and subcategory labels.
- Inspected potential outliers without automatically removing them.

### 3. Basic Exploratory Data Analysis

Analysed product listings by:

- Category
- Brand
- Subcategory
- Quantity and pack size

Created visualisations to identify the most common categories, brands, subcategories, and recorded pack sizes.

### 4. Detailed Exploratory Data Analysis

- Examined price and discount distributions using histograms and boxplots.
- Compared average discount percentages across categories.
- Analysed the number of products, brands, and subcategories within categories.
- Compared DMart Grocery rice listings with regular Grocery rice listings.
- Investigated clothing subcategories and discount patterns.
- Examined brand-level average discounted prices in clothing.
- Identified women's clothing listings with discounts above 50%.

## Key Findings

The following findings are based on the recorded notebook outputs.

### 1. Overall Discount Analysis

The overall mean `DiscountPercent` was approximately **26.02%**.

This describes the average discount percentage across the analysed product listings. It should not be interpreted as an average customer saving or sales-weighted discount.

### 2. Category-Wise Discount Analysis

Average discounts were calculated and sorted by category.

Some categories showed high average discounts, including:

- Smartwatches: approximately 58%
- Backpacks: approximately 51.46%

These results must be interpreted alongside product counts. For example, the Smartwatches category contained only one listing in the recorded output, so its average is not representative of a broad product group.

### 3. DMart Grocery vs Regular Grocery — Rice Comparison

The recorded notebook results showed:

| Metric | DMart Grocery Rice | Regular Grocery Rice |
|---|---:|---:|
| Average original price | ₹437 | ₹348 |
| Average discount | 24% | 22% |

In this comparison, DMart Grocery rice listings had a higher average listed price and average discount than the regular Grocery rice listings.

This is a descriptive comparison of the selected groups. It does not establish why the differences exist, and the exact-match filters should be checked to ensure all intended rice listings are included.

### 4. Clothing Analysis

The clothing analysis included:

- Distribution of men's and women's clothing subcategories.
- Average discount percentage by clothing subcategory.
- Average discounted price by brand.
- Identification of women's clothing listings with discounts above 50%.

These analyses help describe the listed clothing assortment and its pricing patterns. They do not establish actual customer preferences or sales performance.

### 5. Outlier Analysis

The IQR method identified the following potential outlier counts:

| Column | Potential outliers |
|---|---:|
| Price | 455 |
| DiscountedPrice | 460 |
| DiscountPercent | 37 |

The notebook retained these records. An IQR outlier is a statistical flag and is not necessarily an incorrect value.

## Data Quality Notes

The recorded cleaning summary reported:

- Zero missing cells after cleaning.
- Zero exact duplicate rows.
- Zero negative original prices.
- Zero negative discounted prices.
- Zero outlier records removed.

Some missing values were imputed or replaced with placeholders during cleaning. Zero-price records and imputed values may affect discount calculations and should be reviewed before the results are used for decisions.

Category and subcategory mapping decisions can also influence the results and should be documented.

## Conclusion

This project provides a descriptive overview of DMart product listings, category distribution, brand availability, prices, and discount patterns.

The analysis reported an overall mean discount of approximately 26.02% and identified differences in average discounts across categories. It also compared the listed prices and discounts of DMart Grocery rice with regular Grocery rice and explored the men's and women's clothing assortment.

The project demonstrates practical skills in Python-based data cleaning, exploratory data analysis, statistical summaries, and visualisation. The findings should be presented as catalogue-level insights, with appropriate caution around small category sizes, imputed values, and category standardisation.

Because the dataset does not contain transaction-level sales or customer information, it cannot establish actual sales, revenue, demand, or customer buying behaviour.

## Future Improvements

- Build a Power BI dashboard to present the main findings.
- Export important charts and add them to the repository.
- Validate category mappings and discount calculations.
- Include product counts alongside average discount comparisons.
- If transaction-level data becomes available, explore sales and customer behaviour as a separate project.

## How to Run the Project

1. Clone or download this repository.
2. Open `DMart.ipynb` in Google Colab or Jupyter Notebook.
3. Upload the source CSV file if you have permission to use it.
4. Update the dataset path in the notebook.
5. Run the cells from top to bottom.
6. Review the generated tables, charts, and findings.

## Author
Suriyan K
Advanced Data Science & AI

**Data Analysis Project — DMart Product Catalogue**

Skills demonstrated: Python, pandas, NumPy, data cleaning, exploratory data analysis, statistics, data visualisation, and business insight generation.
