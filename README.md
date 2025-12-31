# Machine-Failure-Prediction-using-Sensor-Data
Machine Failure dataset contains sensor data collected from various industrial machines with the aim of predicting machine failures in advance. It includes a variety of sensor readings along with recorded machine failure events, making it ideal for developing predictive maintenance models.

The data represents real-time or near-real-time monitoring of machine operations through multiple sensor types, capturing different aspects of machine health and environmental conditions.

## Features (Columns)
| Feature         | Description                                                 |
| --------------- | ----------------------------------------------------------- |
| **footfall**    | Count of objects/people near the machine                    |
| **tempMode**    | Temperature mode/setting                                    |
| **AQ**          | Air quality index around equipment                          |
| **USS**         | Ultrasonic sensor reading                                   |
| **CS**          | Current sensor data                                         |
| **VOC**         | Volatile Organic Compounds level                            |
| **RP**          | Rotational position (like RPM)                              |
| **IP**          | Input pressure                                              |
| **Temperature** | Operating temperature                                       |
| **fail**        | **Target** — 1 or 0 (failure occurred or not)               |

**Goal**: Predict the ‘fail’ label (0/1) using the sensor inputs.

## Dataset Characteristics
### Data Collection
- Temporal: Time-series sensor readings collected at regular intervals
- Multivariate: Multiple sensor types capturing different aspects of machine health
- Real-world: Contains actual sensor data from industrial equipment

### Data Quality
- Completeness: Check for missing values in sensor readings
- Noise: Real sensor data may contain measurement noise
- Imbalance: Failure events are typically rare (class imbalance expected)

## WorkFlow
1. Data Collection
2. Data Preprocessing / Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Train/Test Split (with stratification for imbalance)
5. Model Training (multiple algorithms)
6. Model Prediction
7. Model Evaluation & Comparison

## Analysis Approaches:
### 1. Exploratory Data Analysis (EDA)
- Distribution analysis of each sensor
- Correlation between sensors
- Comparison of sensor values: failure vs. no failure
- Time series patterns (if timestamps available)

### 2. Feature Engineering
- Rolling statistics (mean, std, max, min over time windows)
- Rate of change (first differences)
- Interaction features (e.g., temperature × VOC)
- Anomaly flags (values beyond threshold)
- Lag features for time dependencies

### 3. Machine Learning Models
- Linear Regression
- Random Forest
- XGBoost

### 4. Evaluation Metrics
- Accuracy: Overall correctness (may be misleading with imbalance)
- Precision: Minimize false alarms
- Recall: Catch all actual failures (critical for safety)
- F1-Score: Balance precision and recall
- ROC-AUC: Overall model discrimination ability
- Confusion Matrix: Understand error types

## Download Dataset
Kaggle Dataset: [https://www.kaggle.com/datasets/umerrtx/machine-failure-prediction-using-sensor-data](https://www.kaggle.com/datasets/umerrtx/machine-failure-prediction-using-sensor-data)
