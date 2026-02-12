# Data Cleaning Documentation (`cleaned.md`)

This document describes the complete step-by-step process followed to clean and prepare the raw flight delay dataset for analysis and KPI reporting.

---

## 1. Raw Dataset Preparation

### Sheet: `Raw_Data (Duplicate Removed)`
- Imported the original raw flight dataset.
- Removed duplicate rows to ensure each flight record was unique.
- This became the starting point for all further cleaning steps.

---

## 2. Tail Number Cleaning

### Sheet: `Cleaned_Tail_Number (39 Rows)`
- Checked the **Tail Number** column for missing or invalid aircraft identifiers.
- Removed rows where tail numbers were blank or incorrectly formatted.
- Ensured all remaining tail numbers were consistent and usable for aircraft-level analysis.

---

## 3. Departure Time Cleaning

### Sheet: `Cleaned_Departure_Time (130 Rows)`
- Inspected the **Departure Time** field.
- Removed or corrected rows with missing, zero, or invalid departure times.
- Standardized the format so departure times could be used in time-based delay analysis.

---

## 4. Taxi-Out Time Cleaning

### Sheet: `Cleaned_Taxi_Out (2 Rows)`
- Verified the **Taxi-Out Time** column for extreme or incorrect values.
- Removed rows with unrealistic taxi-out durations.
- Ensured taxi-out times were valid for operational delay calculations.

---

## 5. Elapsed Time Cleaning

### Sheet: `Cleaned_Elapsed_Time (8 Rows)`
- Checked the **Elapsed Time** column for missing or inconsistent flight durations.
- Removed records with invalid elapsed time values.
- Ensured flight duration data was accurate for delay benchmarking.

---

## 6. Final Dataset Filtering

### Sheet: `Final_Cleaned_Data (Dropped Diverted and Cancelled)`
- Removed flights that were:
  - **Cancelled**
  - **Diverted**
- These records do not represent normal delay behavior and would distort KPI results.
- The remaining dataset represents valid completed flights only.

---

## 7. KPI and Pivot Table Analysis

After cleaning, the dataset was used for analysis and reporting:

### Sheet: `Monthly Average Arrival Delay`
- Calculated average arrival delay grouped by month.
- Used for identifying seasonal delay patterns.

### Sheet: `Average Arrival Delay per Airline`
- Computed airline-wise delay performance.
- Helps compare which airlines are most punctual.

### Sheet: `Total Flights per Airline`
- Counted total flights for each airline.
- Used to understand airline traffic volume and support normalization.

---

## ✅ Final Outcome

The raw dataset was successfully transformed into a structured, accurate, and analysis-ready dataset through:

- Duplicate removal  
- Missing value filtering  
- Time format corrections  
- Invalid record removal  
- Dropping cancelled/diverted flights  
- KPI-ready pivot summaries  

This cleaned dataset forms the foundation for flight delay analytics and prediction modeling.

---
