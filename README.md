# Task_1_Data_Cleaning_and_Processing

## 🧹 Data Cleaning Steps – Medical Appointment No Shows Dataset

This project focuses on cleaning and preprocessing the **Medical Appointment No Shows** dataset to prepare it for analysis or machine learning modeling. The following key data cleaning steps were performed in the `Data_Cleaning.ipynb` notebook:

### 📁 Dataset

* Original dataset file: `Medical Appointment No Shows.csv`

### 🔧 Cleaning Process

1. **Loading the Dataset**

   * Loaded the CSV file using `pandas.read_csv()`.

2. **Standardizing Column Headers**

   * Converted all column names to lowercase.
   * Replaced spaces and hyphens with underscores for consistency.
   * Corrected typos in column names:

     * `hipertension` ➝ `hypertension`
     * `handcap` ➝ `handicap`
     * `patientid` ➝ `patient_id`
     * `appointmentid` ➝ `appointment_id`
     * `appointmentday` ➝ `appointment_day`

3. **Converting Datetime Columns**

   * Converted `scheduled_day` and `appointment_day` to `datetime64[ns]` type using `pd.to_datetime()`.
   * Extracted only the **date** part from the `appointment_day` column.
   * Created a new column `scheduled_time` to capture the **time** portion from the `scheduled_day` column.

4. **Data Type Standardization**

   * Ensured all datetime columns are correctly typed for time-based operations and analysis.

5. **Exporting the Cleaned Data**

   * Saved the cleaned DataFrame to a new CSV file: `Cleaned_Medical_Appointment_Data.csv` using `df.to_csv(index=False)`.

### 🧪 Technologies Used

* Python 🐍
* Pandas 🐼
* Jupyter Notebook 📓


