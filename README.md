[README.md](https://github.com/user-attachments/files/23658609/README.md)

# Exploratory Data Analysis (EDA) of Sensor Data

## Introduction
This repository contains an Exploratory Data Analysis (EDA) of sensor data collected over several days. The analysis includes unzipping the data, loading multiple CSV files into a single DataFrame, visualizing trends of key environmental parameters (temperature, humidity, light), analyzing correlations between these variables, identifying patterns like day-night cycles, and computing basic statistics for all sensor readings.

## EDA Summary

### Data Analysis Key Findings

*   **Data Loading and Structure**: Seven CSV files were successfully loaded and concatenated into a single DataFrame `df` comprising 120,960 entries with no missing values. The 'timestamp' column was correctly parsed as datetime objects and the data sorted chronologically.
*   **Time-Series Trends**:
    *   **Temperature**: The temperature data shows fluctuations over time, remaining within a range of 20.0°C to 25.0°C.
    *   **Humidity**: Humidity also exhibits variations, ranging from 40.0% to 60.0%.
    *   **Light**: Light intensity clearly demonstrates pronounced day-night cycles, fluctuating between 100.0 Lux and 999.99 Lux.
*   **Correlations**:
    *   **Temperature and Humidity**: Show a very weak positive correlation (0.003655).
    *   **Temperature and Light**: Exhibit a very weak negative correlation (-0.000423).
    *   **Humidity and Light**: Also have a very weak negative correlation (-0.001196).
*   **Patterns**:
    *   **Day-Night Cycles**: The light intensity plot vividly illustrates clear day-night cycles with periodic increases and decreases.
    *   **Humidity vs. Temperature**: The scatter plot indicates no strong linear or inverse relationship between humidity and temperature, supporting the weak correlation coefficient.
*   **Basic Statistics**:
    *   **Temperature**: Mean: 22.50°C, Min: 20.0°C, Max: 25.00°C, Variance: 2.08.
    *   **Humidity**: Mean: 50.03%, Min: 40.0%, Max: 60.00%, Variance: 33.26.
    *   **Light**: Mean: 549.10 Lux, Min: 100.0 Lux, Max: 999.99 Lux, Variance: 67457.73.
    *   **pH**: Mean: 7.00, Min: 6.0, Max: 8.00, Variance: 0.33.
    *   **Electrical Conductivity (EC)**: Mean: 1.25, Min: 0.5, Max: 2.00, Variance: 0.19.

### Insights or Next Steps

*   The very weak correlations between temperature, humidity, and light suggest that these environmental factors might be largely independent of each other in the observed system, or their interdependencies are non-linear or lagged, which warrants further investigation.
*   Further analysis could involve decomposing the time-series data to identify seasonality and trends more precisely, especially for temperature and humidity, and exploring potential external factors influencing these variables beyond the current dataset.

## Visualizations

### Trends of Temperature, Humidity, and Light Over Time
![Trends of Temperature, Humidity, and Light](plots/trends_temperature_humidity_light.png)

### Correlation Heatmap of Temperature, Humidity, and Light
![Correlation Heatmap](plots/correlation_heatmap.png)

### Light Intensity Over Time (Day-Night Cycles)
![Light Day-Night Cycles](plots/day_night_cycles.png)

### Relationship Between Humidity and Temperature
![Humidity vs. Temperature Scatter Plot](plots/humidity_temperature_scatter.png)
