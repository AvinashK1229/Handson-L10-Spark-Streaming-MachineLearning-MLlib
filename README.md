
# Spark Structured Streaming with MLlib - Real-Time Ride-Sharing Analytics

## Overview
Real-time analytics pipeline for ride-sharing platform using Apache Spark Structured Streaming and MLlib for fare prediction and trend analysis.

## Project Structure
```
├── models/
│   ├── fare_model/
│   └── fare_trend_model_v2/
├── data_generator.py
├── task4.py
├── task5.py
├── training-dataset.csv
└── README.md
```

## Tasks

### Task 4: Real-Time Fare Prediction
- Trains LinearRegression model on `distance_km` → `fare_amount`
- Predicts fares for streaming rides in real-time
- Calculates deviation to detect anomalies

### Task 5: Time-Based Fare Trend Prediction
- Aggregates data into 5-minute windows
- Engineers temporal features: `hour_of_day`, `minute_of_hour`
- Predicts average fare trends over time windows

## How to Run

1. **Start Data Generator**
```bash
python data_generator.py
```

2. **Run Task 4**
```bash
spark-submit task4.py
```

3. **Run Task 5**
```bash
spark-submit task5.py
```

## Outputs

### Task 4: Fare Prediction



<img width="1017" height="629" alt="Screenshot 2025-10-21 232327" src="https://github.com/user-attachments/assets/a86a37b9-7435-4cfe-9aad-a6d6a973e81e" />



### Task 5: Fare Trend Prediction

<img width="1156" height="282" alt="Screenshot 2025-10-21 232415" src="https://github.com/user-attachments/assets/7eae0594-ed52-4c91-b2e7-ed271a3a3155" />

## Tech Stack
- Apache Spark (Structured Streaming + MLlib)
- Python 3.x
- LinearRegression Model
- Socket Streaming (localhost:9999)


