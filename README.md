# Data Analyst Internship – Task 1
## Data Cleaning and Preprocessing: Mall Customers

The supplied internship task asks for data cleaning and preprocessing, including handling missing values, duplicate rows, standardized text, consistent formats, clean column headers, and correct data types. It also requires a cleaned dataset and a short summary of changes. 

### Dataset used
`Mall_Customers.csv` from the user's uploaded `archive.zip`.

### Audit of the supplied data
- Rows: **200**
- Columns: **5**
- Missing cells: **0**
- Exact duplicate rows: **0**
- Duplicate CustomerID values: **0**
- Gender categories: **['Female', 'Male']**
- Numeric fields are already stored as integer types.
- Age range: **18–70**
- Annual income range: **15–137**
- Spending score range: **1–99**

### Cleaning performed
1. Removed whitespace from column headers.
2. Converted headers to lowercase, underscore-separated names:
   - `CustomerID` → `customerid`
   - `Gender` → `gender`
   - `Age` → `age`
   - `Annual Income (k$)` → `annual_income_k`
   - `Spending Score (1-100)` → `spending_score_1_100`
3. Standardized gender text using strip + title case.
4. Explicitly converted numeric columns to numeric data types.
5. Checked for duplicate rows and duplicate CustomerIDs.
6. Checked for missing values. **No missing values were present, so no values were artificially imputed.**
7. Checked logical ranges for customer ID, age, income, and spending score.
8. Saved the cleaned dataset as a separate CSV.

### Important finding
This particular supplied dataset is already very clean: it has **no nulls, no duplicate rows, and no duplicate CustomerIDs**. Therefore, the correct data-cleaning approach is to document those checks rather than inventing missing or duplicate records.

### Deliverables
- `data/Mall_Customers_Cleaned.csv`
- `data/data_quality_report.csv`
- `src/clean_mall_customers.py`
- `README.md`
- `INTERVIEW_ANSWERS.md`
- `requirements.txt`
