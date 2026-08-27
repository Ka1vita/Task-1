# Interview Questions – Task 1

### 1. What are missing values and how do you handle them?
Missing values are observations where data is unavailable or empty. I first identify them with `isnull().sum()`. Depending on the data, I may remove records or fill values using mean, median, mode, or a business rule. In this Mall Customers dataset, there are no missing values, so no imputation is required.

### 2. How do you treat duplicate records?
I identify duplicates with `duplicated()` and remove them using `drop_duplicates()`. For this dataset I also check `CustomerID`, because it should uniquely identify each customer. The supplied file has no duplicate CustomerIDs.

### 3. Difference between `dropna()` and `fillna()` in Pandas?
`dropna()` removes rows or columns containing missing values. `fillna()` replaces missing values with a selected value such as a median, mean, mode, or constant.

### 4. What is outlier treatment and why is it important?
Outlier treatment means identifying unusually high or low observations and deciding whether they are valid or errors. It is important because extreme values can affect averages, visualizations, statistical analysis, and machine-learning models. For this task, I performed range validation but did not remove valid observations just because they are relatively high or low.

### 5. Explain the process of standardizing data.
Standardization makes data consistent. Examples include cleaning column names, removing extra spaces, using consistent capitalization for categories, converting dates to one format, and ensuring columns use appropriate data types.

### 6. How do you handle inconsistent data formats such as date/time?
I first identify the formats present, then parse them with an appropriate Pandas function such as `pd.to_datetime()` and validate failed conversions. This dataset does not contain a date/time column.

### 7. What are common data cleaning challenges?
Common challenges include missing values, duplicates, inconsistent category labels, mixed formats, incorrect data types, invalid values, outliers, encoding issues, and unclear business rules.

### 8. How can you check data quality?
I check row/column counts, null counts, duplicate records, duplicate IDs, data types, unique categories, valid ranges, and business-rule constraints. I also compare the dataset before and after cleaning.
