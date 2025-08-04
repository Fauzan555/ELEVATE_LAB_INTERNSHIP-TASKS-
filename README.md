# 🧹 Amazon Sales Data Cleaning - Elevate Lab Internship

This project demonstrates a structured data cleaning pipeline using a real-world e-commerce dataset from Amazon. The task was completed as part of the Elevate Lab Internship assignment and focuses on preparing messy data for further analysis and machine learning applications.

## 🧠 Objective

The goal of this task is to perform data cleaning on an Amazon product and review dataset, including:
- Identifying and handling missing values
- Correcting data types
- Standardizing text fields
- Removing duplicates
- Making the dataset analysis-ready

---

## 📊 Dataset Overview

The dataset includes Amazon product and user review information with the following key columns:

- `product_id`, `product_name`, `category`
- `discounted_price`, `actual_price`, `discount_percentage`
- `rating`, `rating_count`
- `user_id`, `user_name`, `review_title`, `review_content`
- `img_link`, `product_link`, `review_id`
- `about_product`

---

## 🔧 Data Cleaning Steps Performed

### ✅ 1. Handling Missing Values
- Used `.isnull().sum()` to identify missing values.
- Found 2 missing values in the `rating_count` column.
- Converted `rating_count` to numeric (it was object/string).
- Imputed missing values using the **median** of the column.

### ✅ 2. Detecting and Removing Duplicates
- Checked for duplicates using `.duplicated()` — **none found**.

### ✅ 3. Identifying and Converting Data Types
- Identified `discounted_price`, `actual_price`, `discount_percentage`, and `rating` as text (object) columns that should be numeric.
- Used `pd.to_numeric(..., errors='coerce')` to convert them.
- Confirmed all were converted to `float64`.

### ✅ 4. Text Cleaning and Standardization
Applied the following transformations to all text-based columns:
- Converted all text to lowercase
- Trimmed leading/trailing whitespaces
- Replaced multiple spaces with a single space
- Removed special characters using regular expressions

### ✅ 5. Column Name Standardization
- Renamed all columns to:
  - Lowercase
  - Snake_case (`_`)
  - Removed special characters and spaces

---

## 📈 Final Output

The dataset is now clean, consistent, and ready for further analysis or modeling tasks such as:
- Sentiment analysis on `review_content`
- Rating prediction models
- Product recommendation systems

---

## 🚀 Tools & Libraries Used

- Python 3.x
- Pandas
- NumPy
- Jupyter Notebook

---
