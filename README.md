# 🏢 Apartment Market Exploratory Data Analysis (EDA)

This project presents an exploratory data analysis (EDA) of apartment listings in Ukraine using Python.

The analysis focuses on pricing patterns, apartment characteristics, data quality issues, and the structure of price distributions, with a particular emphasis on Kyiv and surrounding cities.

The project was originally developed as part of a data analytics course and later adapted and structured for portfolio presentation on GitHub.

---

## Dataset description

The dataset contains structured information about apartments listed for sale, including:

- location (city / locality)
- apartment characteristics (total area, living area, kitchen area, number of rooms)
- floor and total number of floors
- price information
- additional features (balcony, ceiling height, studio format)

The dataset is stored locally in the `data/` directory and loaded using **pandas**.

---

## Research questions

The analysis addresses the following questions:

- What is the cost per square meter of apartments?
- What number of rooms is most common among apartments sold in Kyiv?
- What is the average price of a one-room apartment in Irpin?
- How popular are studio apartments?
- Is there evidence of a multimodal distribution of apartment prices per square meter in Kyiv?
- What data quality issues and inconsistencies are present in the dataset?

---

## Data preprocessing and feature engineering

Key preprocessing steps include:

- removal of irrelevant or empty columns
- normalization of location names
- handling missing and zero values
- conversion of date fields to datetime format
- creation of a new feature: **price per square meter**

Example:

```python
apartments_df['price_per_m2'] = apartments_df['last_price'] / apartments_df['total_area']
