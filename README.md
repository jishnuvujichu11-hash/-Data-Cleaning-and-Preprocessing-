#  Data Cleaning Project — Medical Dataset (May 2016)

##  Overview
This project focuses on **data cleaning and preprocessing** of the dataset `medical-May-2016.csv` using **Python (pandas)**.  
It demonstrates how to clean, format, and prepare raw data for analysis or machine learning.

---

##  Steps Performed

### 1️ Load the Dataset
- Import the CSV file using `pandas.read_csv()`
- Preview the data using `.head()`

### 2️ Identify and Handle Missing Values
- Check for missing data using `.isnull().sum()`
- Handle missing data by removing (`.dropna()`) or filling (`.fillna()`) values

### 3️ Remove Duplicate Records
- Detect duplicate rows with `.duplicated()`
- Remove duplicates using `.drop_duplicates()`

### 4️ Standardize Text Values
- Clean inconsistent text values such as gender, country, etc.
- Example: converting `M`, `m`, `male.` → `male`

### 5️ Convert Date Formats
- Convert date columns to a consistent format (`dd-mm-yyyy`)
- Use `pd.to_datetime()` for date parsing

### 6️ Rename Column Headers
- Convert column names to lowercase  
- Replace spaces with underscores (`_`)  
- Remove special characters for uniformity

### 7️ Fix Data Types
- Ensure numeric columns are `int` or `float`
- Convert date columns to `datetime`
- Use `.astype()` and `pd.to_numeric()` for type correction

### 8️ Export the Cleaned Dataset
- Save the final cleaned data as:
  ```python
  df.to_csv("medical-May-2016_cleaned.csv", index=False)

