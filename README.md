# Titanic Dataset — Data Cleaning and Exploratory Data Analysis

## Project Overview

This project performs data acquisition, data cleaning, preprocessing, and exploratory data analysis (EDA) on the Titanic passenger dataset using Python.

The project focuses on identifying and handling missing values, checking duplicate records, examining the dataset structure, and exploring patterns related to passenger survival.

## Objectives

- Acquire and load a publicly available dataset.
- Inspect the structure and quality of the data.
- Identify and handle missing values.
- Check for duplicate records.
- Perform descriptive statistical analysis.
- Create visualizations to identify patterns and relationships.
- Summarize the key findings from the exploratory analysis.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- VS Code

## Project Structure

```text
Data_Science_Titanic/
├── data/
│   └── traititanic.csv
├── notebooks/
│   └── Titanic_Analysis.ipynb
├── visualizations/
│   ├── 01_survival_distribution.png
│   ├── 02_survival_by_sex.png
│   ├── 03_missing_values.png
│   └── 04_correlation_heatmap.png
├── report/
├── .gitignore
├── README.md
└── requirements.txt
```

## Data Cleaning

The dataset was inspected for missing values and duplicate records.

The following cleaning steps were performed:

- `Age`: 177 missing values were replaced with the median age of 28.0.
- `Embarked`: 2 missing values were replaced with the mode, `S`.
- `Cabin`: 687 values were missing, so the column was removed because of its high proportion of missing data.
- Duplicate records: No duplicate rows were found.

After cleaning, the dataset contained 891 rows and 11 columns with no remaining missing values.

## Exploratory Data Analysis

The analysis explored passenger survival using:

- Overall survival distribution
- Survival by sex
- Survival by passenger class
- Missing-value distribution
- Correlation between numerical variables

### Key Findings

- 342 of 891 passengers survived, representing approximately 38.4% of the dataset.
- Approximately 74.2% of female passengers survived, compared with 18.9% of male passengers.
- Approximately 63.0% of first-class passengers survived, compared with 47.3% of second-class and 24.2% of third-class passengers.
- `Pclass` had the strongest negative correlation with `Survived` among the numeric variables, with a correlation of -0.338.
- `Fare` had a positive correlation with `Survived` of 0.257.
- Correlation describes an association and does not by itself establish causation.

## Visualizations

The project includes four saved visualizations:

1. Survival distribution
2. Survival by sex
3. Missing values before cleaning
4. Correlation heatmap

The visualization files are available in the `visualizations/` directory.

## How to Run

Clone or download the repository and navigate to the project directory.

Create and activate a virtual environment:

```bash
python -m venv .venv


## On Windows PowerShell:

.venv\Scripts\Activate.ps1

## Install the required packages:

pip install -r requirements.txt

## Open the Jupyter Notebook:

jupyter notebook

## Then open:

notebooks/Titanic_Analysis.ipynb