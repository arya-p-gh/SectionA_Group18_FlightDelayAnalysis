# Flight Delay Operational Performance Analysis  
## README

---

## 1. Project Overview  

This project analyzes flight delay patterns across airlines, weekdays, and airports to identify structural inefficiencies within airline operations.

The original dataset consisted of over **1,050,000 flight-level records across 22 operational variables**. A statistically randomized sample of **5,000 flights** was generated using Google Colab to ensure computational feasibility within Google Sheets while preserving statistical representativeness.

The dataset was systematically cleaned, validated, and filtered to include only completed flights. The objective of this analysis is to detect delay concentration patterns and provide actionable insights for operational optimization and performance monitoring.

---

## 2. Data Dictionary  

The dataset contains 22 structured variables. Key analytical fields are summarized below:

| Column Name        | Description                                      | Type        |
|--------------------|--------------------------------------------------|------------|
| Airline            | Airline carrier code                             | Categorical |
| Tail Number        | Aircraft identifier                              | Categorical |
| Origin Airport     | Departure airport code                           | Categorical |
| Destination Airport| Arrival airport code                             | Categorical |
| DayOfWeek          | Numeric weekday (1–7)                            | Numeric |
| Departure Time     | Actual departure time                            | Time |
| Arrival Time       | Actual arrival time                              | Time |
| Departure Delay    | Delay in departure (minutes)                     | Numeric |
| Arrival Delay      | Delay in arrival (minutes)                       | Numeric |
| Taxi-Out Time      | Time from gate to runway (minutes)               | Numeric |
| Elapsed Time       | Total flight duration (minutes)                  | Numeric |
| Cancelled          | Flight cancellation indicator (0/1)              | Binary |
| Diverted           | Flight diversion indicator (0/1)                 | Binary |
| Distance           | Flight distance (miles/km)                       | Numeric |

Derived variables created during analysis include:

- Delay Category (On-Time / Minor / Major)  
- Delay Flag (Binary Indicator)  
- Weekend Indicator  
- Daily Aggregations  

---

## 3. Cleaning Notes  

The cleaning process was executed in structured stages, with each stage documented in separate sheets:

### Raw Data
- Imported 5,000 randomly sampled records.
- Removed duplicate entries to ensure record uniqueness.

### Tail Number Validation
- Removed rows with missing or invalid aircraft identifiers (39 records removed).

### Departure Time Cleaning
- Removed rows with missing, zero, or invalid departure times (130 records removed).
- Standardized time formats for consistency.

### Taxi-Out Time Validation
- Removed unrealistic taxi-out duration values (2 records removed).

### Elapsed Time Validation
- Removed records with invalid flight duration values (8 records removed).

### Final Filtering
- Removed cancelled and diverted flights.
- Retained only valid, completed operational records.

The final dataset is structured, consistent, and analysis-ready.

---

## 4. Key Insights  

- Delay patterns vary significantly across airlines, indicating carrier-specific operational efficiency differences.
- Monday exhibits the highest average delay levels, suggesting peak-demand congestion effects.
- Delay concentration is uneven across airports, with specific hubs acting as operational bottlenecks.
- Delay distribution is positively skewed, with extreme values influencing overall averages.
- Traffic volume alone does not fully explain delay performance; operational management capability plays a significant role.

Overall, delays are structurally concentrated rather than randomly distributed.

---

## 5. Dashboard Summary  

Three integrated dashboards were developed in Google Sheets:

### Airline Performance Dashboard
- Average Arrival and Departure Delay by Airline
- Total Flights per Airline
- Top 5 Airline Performance Comparison
- Interactive Airline Filter

### Day-of-Week Analysis Dashboard
- Average Delay by Weekday
- Comparative Arrival vs Departure Trends
- Identification of high-congestion days

### Airport Performance Dashboard
- Average Arrival Delay per Airport
- Average Departure Delay per Airport
- Bottleneck Identification through delay concentration

The dashboard structure enables progressive exploration from executive-level KPIs to granular operational insights. It functions as a decision-support system for continuous performance monitoring and operational optimization.

---

## Final Outcome  

The project successfully transformed raw operational flight records into a structured analytical framework.  

Through systematic cleaning, KPI design, pivot analysis, and dashboard development, the dataset was converted into actionable aviation performance intelligence capable of supporting strategic operational decisions.
