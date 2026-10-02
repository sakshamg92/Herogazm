# Student Data Cleaning — Pandas

## Overview

This project demonstrates the cleaning and preparation of a student dataset using **Python, Pandas, and NumPy**.

The original dataset contains common data-quality issues such as duplicate records, missing values, inconsistent text formatting, and invalid numerical values. The goal is to transform the raw data into a clean and analysis-ready dataset.

## Dataset

The dataset contains student information including:

- Name
- Age
- Gender
- City
- Maths score
- Physics score
- Attendance
- Email

## Data Cleaning Process

The following data-quality issues were identified and addressed:

1. **Duplicate Records**
   - Identified and removed duplicate student records.

2. **Text Standardization**
   - Removed leading/trailing whitespace.
   - Standardized `Gender` and `City` values for consistent representation.

3. **Missing Values**
   - Numerical missing values were handled using the column median.
   - Missing categorical/text values were replaced with `Unknown`.

4. **Invalid Values**
   - Identified invalid age values.
   - Validated attendance and academic scores against their expected `0–100` range.
   - Invalid numerical values were treated as missing and handled appropriately.

5. **Data Types**
   - Converted categorical fields such as `Gender` and `City` to Pandas `category` dtype.

6. **Validation**
   - Verified that duplicate records were removed.
   - Checked for remaining missing values.
   - Validated numerical ranges and data types.

## Output

The cleaned dataset is saved as:

```text
Students_cleaned.csv
```

The cleaned file is ready for **exploratory data analysis, visualization, and further statistical analysis**.

## Tools & Technologies

- Python
- Pandas
- NumPy
- VS Code (Jupyter Notebook Extention)

## Project Structure

```text
Task-01-10-26/
│
├── Students_messy.csv
├── Students_cleaned.csv
├── Students_messy.ipynb
└── README.md
```

## Reproducibility

To reproduce the cleaning process:

```python
import pandas as pd
import numpy as np

df = pd.read_csv("Students_messy.csv")
```

Run the cleaning workflow and export the final DataFrame using:

```python
df.to_csv("Students_cleaned.csv", index=False)
```
