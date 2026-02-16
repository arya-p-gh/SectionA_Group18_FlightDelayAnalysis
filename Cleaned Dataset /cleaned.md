# Data Cleaning Documentation (`cleaned.md`)

This document describes the complete step-by-step process followed to sample, clean, and prepare the raw flight delay dataset for analysis and KPI reporting.

---

## 0. Dataset Sampling (Initial Step)

### Environment: `Google Colab`
- The original dataset contained approximately **10.5 lakh (1,050,000) flight records**.
- To ensure efficient processing and faster iteration, a **random sample of 5,000 records** was extracted using Google Colab.
- Random sampling was performed without bias to maintain representativeness across airlines, routes, and time periods.
- This 5,000-record dataset became the working dataset for all subsequent cleaning and analysis.

---

## 1. Raw Dataset Preparation

### Sheet: `Raw_Data (Duplicate Removed)`
- Imported the sampled dataset (5,000 records).
- Removed duplicate rows to ensure each flight record was unique.
- This became the starting point for all further cleaning steps.

---

## 2. Tail Number Cleaning

### Sheet: `Cleaned_Tail_Number (39 Rows Removed)`
- Checked the **Tail Number** column for missing or invalid aircraft identifiers.
- Removed rows where tail numbers were blank or incorrectly formatted.
- Ensured all remaining tail numbers were consistent and usable for aircraft-level analysis.

---

## 3. Departure Time Cleaning

### Sheet: `Cleaned_Departure_Time (130 Rows Removed)`
- Inspected the **Departure Time** field.
- Removed or corrected rows with missing, zero, or invalid departure times.
- Standardized the format so departure times could be used in time-based delay analysis.

---

## 4. Taxi-Out Time Cleaning

### Sheet: `Cleaned_Taxi_Out (2 Rows Removed)`
- Verified the **Taxi-Out Time** column for extreme or incorrect values.
- Removed rows with unrealistic taxi-out durations.
- Ensured taxi-out times were valid for operational delay calculations.

---

## 5. Elapsed Time Cleaning

### Sheet: `Cleaned_Elapsed_Time (8 Rows Removed)`
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

The original dataset (~10.5 lakh records) was:

- Randomly sampled to 5,000 records using Google Colab  
- Deduplicated  
- Cleaned for missing and invalid values  
- Time-standardized  
- Filtered to remove cancelled/diverted flights  
- Structured for KPI computation  

The final dataset is structured, accurate, and analysis-ready, forming the foundation for:

- Flight delay analytics  
- Airline performance benchmarking  
- Seasonal trend analysis  
- Predictive modeling workflows  
