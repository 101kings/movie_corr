# 🎬 Movie Dataset Cleaning & Correlation Analysis

This project focuses on cleaning a movie dataset and performing exploratory data analysis using Python (Pandas, Matplotlib, and Seaborn). It includes handling missing data, feature extraction, and generating a correlation heatmap to uncover relationships between numerical features.

## 📌 Objective

- Clean raw movie data for accurate analysis.
- Handle missing values and convert data types appropriately.
- Extract useful features (e.g., release year).
- Find and visualize correlations using a heatmap.

## 🧰 Tools & Libraries

- Python (Jupyter Notebook)
- Pandas
- NumPy
- Seaborn
- Matplotlib

## 🧼 Data Cleaning Steps

- **Missing Values**:  
  - Dropped rows with missing values in essential columns like `released`.
  - Handled missing numerical data (e.g., `budget`) using imputation where necessary.

- **Data Type Conversion**:  
  - Converted `budget` to integer (`int64`).
  - Extracted release year from string-type `released` column.

- **Feature Engineering**:  
  - Created a new column `year_correct` by slicing the first 4 characters of `released`.

- **Duplicate Removal**:  
  - Checked for and removed duplicate records using `df.duplicated()`.

## 📊 Correlation Analysis

- Selected only numeric columns using `df.corr()`.
- Generated a correlation matrix.
- Created a **Seaborn heatmap** with the following customizations:
  - `square=True` for square cells.
  - `annot=True` to show correlation coefficients.
  - `cmap='Blues'` for blue color gradient.

## 📈 Key Insights

- Strong positive correlation found between `budget`, `gross`, and `votes`.
- Feature cleaning significantly improved dataset quality.
- Correlation matrix helped visualize which variables were most related.

## 📂 How to Use

1. Load the dataset into a Pandas DataFrame.
2. Follow the notebook cells to clean and prepare the data.
3. Run the heatmap cell to visualize correlations.
4. Adjust thresholds or filters to explore relationships further.

## 📎 File Overview

- movie_correlation.ipynb`: Main Jupyter notebook with all cleaning and visualization steps.
- `README.md`: Project description and guide (this file).

## ✅ Conclusion

This project demonstrates how to clean real-world movie data, handle common issues like missing or malformed values, and use correlation analysis for EDA. It is a good foundation for deeper insights, modeling, or recommendation systems.
