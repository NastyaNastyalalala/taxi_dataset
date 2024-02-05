# 🚀 Taxi DataSet - regression analysis

This repository contains research for regression analysis use case.

Task: Predict the duration of a taxi ride.

## DATA Review
| Field name | Overview |
| ------ | ------ |
| id | Trip ID |
| vendor_id | ID of the company carrying out transportation |
| pickup_datetime | Trip start timecode |
| dropoff_datetime | End of trip timecode |
| passenger_count | Number of passengers |
| pickup_longitude | Longitude of the point where the trip started |
| pickup_latitude | Latitude of the point where the trip started |
| dropoff_longitude | Longitude of the point where the trip ended |
| dropoff_latitude | Latitude of the point where the trip ended |
| store_and_fwd_flag | Yes/No: Was information saved in the vehicle's memory due to a loss of connection to the server? |

Target - trip duration

## Brief Overview of the Files:
### 1. requirements.txt
Before running code locally please install dependancies from requirements.txt

### 2. research/taxi_dataset.ipynb
Main research file

### Metrics: MSLE

### Results:
1. EDA
2. Added new featues based on research 'anomaly', 'traffic_jam'
3. Convert 'pickup_longitude', 'pickup_latitude', 'dropoff_longitude', 'dropoff_latitude' the geographic distance 'distance_km'.
4. Processing categorical features(mean-target encoding, one-hot encoding)
5. Model: Linear Regression
6. Cross Validation

As a result, by removing outliers, it was possible to significantly improve the quality, but you need to understand that if the new data contains similar outliers, the model will not be able to cope with them well.

### interesting patterns that were discovered:
- the number of trips in a certain period of time and the average target value corresponding to this period are strongly and positively related
- the rush hour almost always occurs during working hours on almost any day of the week, around 13-15 hours.
- the heaviest months (with the highest target values on average by day of the week): May and June
- the distribution of the target variable for each day of the week is different.




