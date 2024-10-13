# Anomaly Detection in Time Series Data

This repository contains Jupyter notebooks and Python scripts for detecting anomalies in stock price data using a Long Short-Term Memory (LSTM) model. The project focuses on identifying unusual patterns in the stock prices of Siemens Healthineers AG, offering insights that could indicate market anomalies or irregular behaviors in stock performance.

### Dataset Source:

The dataset used for this project is based on historical stock price data for Siemens Healthineers AG. It includes the 'Close' prices for a specified period, which are used to train the anomaly detection model. The dataset can be found in the `SHL_data.csv` file within this repository and can also be downloaded from Yahoo Finance.

### Key Features:

- **Data Preprocessing**: Loaded and visualized stock price data to understand trends over time.
- **Time Series Transformation**: Prepared the data for LSTM modeling by creating time-windowed sequences.
- **LSTM Model**: Implemented an LSTM-based model for time series analysis and anomaly detection.
- **Anomaly Detection**: Detected anomalies using two approaches:
  - Based on the 80th percentile of training errors.
  - Based on a slight change threshold for detecting even small irregularities in stock price.
- **Visualization**: Visualized stock prices along with detected anomalies using Seaborn and Matplotlib.

### Technologies Used:

- **Python**: Used for data preprocessing, model training, and anomaly detection.
- **TensorFlow & Keras**: Employed for building and training the LSTM model.
- **Pandas**: Utilized for data manipulation and sequence generation.
- **Matplotlib & Seaborn**: Used for visualizing stock trends and anomalies.
- **Scikit-learn**: Applied `MinMaxScaler` for normalizing the dataset.

### Data Preprocessing:

- Loaded the historical stock price data from `SHL_data.csv`.
- Normalized the 'Close' prices using `MinMaxScaler` to prepare the data for LSTM modeling.
- Split the dataset into training and testing sets based on a specified date.

### Model Implementation:

- Built an LSTM model with multiple layers, including dropout and batch normalization for regularization.
- Trained the model using the training dataset, with early stopping and learning rate reduction callbacks.
- Evaluated the model's performance by calculating Mean Absolute Error (MAE) on the training data.

### Anomaly Detection:

- Computed the 80th percentile of MAE on training data to set a threshold for anomaly detection.
- Created a second threshold based on slight changes in prediction errors to detect subtle anomalies.
- Identified anomalies in the test dataset based on these thresholds and plotted them over time.

### Visualizations:

- Visualized stock prices along with detected anomalies using:
  - **80th percentile threshold**: Highlighted significant anomalies in red.
  - **Slight change threshold**: Visualized smaller irregularities in stock price behavior.
