# Predicting Rainfall based on time series data

The dataset consisted of over 300 records of rainfall and other climate regressor data from January 2023 to Novemeber. The goal was to predict the future rainfall probabilities based on the trends/ patterns identified from this dataset. 

| Statistic  | Date                  | Avg Temperature | Humidity | Avg Wind Speed | Rain or Not | Cloud Cover | Pressure  |
|------------|-----------------------|----------------|----------|----------------|-------------|-------------|-----------|
| Count      | 311                   | 296.00         | 296.00   | 296.00         | 311.00      | 296.00      | 311.00    |
| Mean       | 2023-06-05 00:00:00    | 25.98          | 55.04    | 7.56           | 0.64        | 49.83       | 1001.06   |
| Min        | 2023-01-01 00:00:00    | 15.00          | 30.00    | 0.07           | 0.00        | 0.32        | 951.24    |
| 25%        | 2023-03-19 12:00:00    | 20.27          | 34.28    | 3.55           | 0.00        | 24.53       | 975.76    |
| 50%        | 2023-06-05 00:00:00    | 27.18          | 56.76    | 7.33           | 1.00        | 50.73       | 1001.94   |
| 75%        | 2023-08-21 12:00:00    | 32.20          | 72.19    | 11.05          | 1.00        | 76.05       | 1026.58   |
| Max        | 2023-11-07 00:00:00    | 35.00          | 90.00    | 56.64          | 1.00        | 99.83       | 1049.54   |
| Std        | NaN                    | 6.80           | 19.22    | 5.34           | 0.48        | 29.01       | 28.84     |


The dataset had no duplicate records but feature values for 15 records were found to be missing. they were implied using time based interpolation. Plus the the target column, Rain or Not was as 'Rain' and 'No Rain'. These values were label encoded as binary features. 
Time series plots revealed that features such as temperature and humidity clearly showed some seasonal variations. A spike of wind speed was also identified here as an outlier and was capped to reduce it's anomalistic impact on the output.

multiple models were tested with varying settings to test out their robustness. 
