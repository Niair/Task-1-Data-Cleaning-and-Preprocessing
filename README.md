# Task1: Data Cleaning and Preprocessing

## 📌 Project Overview

This project demonstrates **advanced data cleaning and preprocessing** techniques using both **Pandas** and **Scikit-learn** libraries. It is part of a broader data science workflow, focusing on transforming raw marketing customer data into a machine learning-ready format.

## 📂 Dataset Information

The dataset includes customer demographics and purchasing behaviour with the following features:
- Demographics (e.g., `year_birth`, `education`, `marital_status`, `income`)
- Purchase history (e.g., `mntwines`, `mntfruits`, `mntmeatproducts`, etc.)
- Web and store interaction metrics
- Campaign responses and complaints

## 🔧 Key Tasks Performed

### ✅ Data Cleaning
- Converted column names to lowercase and snake_case
- Converted `dt_customer` column to `datetime`
- Categorical conversion for `education` and `marital_status`
- Missing value handling (if any)

### ✅ Feature Engineering
- Created new column: `customer_days` = days since enrollment
- Removed `id`, `dt_customer`, `z_costcontact`, and `z_revenue` as they are not useful for modeling

### ✅ Preprocessing Pipeline
Implemented a **Scikit-learn `ColumnTransformer` pipeline**:
- **Numerical Features**: Standardized using `StandardScaler`
- **Categorical Features**: Encoded using `OneHotEncoder`
- Combined both pipelines using `ColumnTransformer` for clean, reusable code

### ✅ Export
- Exported final cleaned and transformed dataset to `processed_data.csv`

## 🧪 Libraries Used
- `pandas`
- `numpy`
- `scikit-learn`

## 📝 How to Run

1. Clone the repository:
   ```
   git clone https://github.com/Niair/Task1_Data_Cleaning_and_Preprocessing.git
   cd Task1_Data_Cleaning_and_Preprocessing

2. Install the requirements:
   ```
   pip install -r requirements.txt

3. Run the Jupyter Notebook or script:
   ```
   jupyter notebook Task1_Data_Cleaning_and_Preprocessing.ipynb

4. The processed data will be saved as:
   ```
   processed_data.csv

## 📁 File Structure
```
Task1_(Data_Cleaning_and_Preprocessing)/
│
├── data/
│   ├── raw_data/
│   │   └── marketing_campaign.csv                      # Original unprocessed dataset
│   ├── processed_data/
│   │   └── processed_data.csv                          # Final cleaned and preprocessed data
│
├── notebooks/
│   └── Task1_(Data _Cleaning_and_Preprocessing).ipynb  # Jupyter Notebook for cleaning steps
│
├── .gitignore
├── README.md
├── requirements.txt
