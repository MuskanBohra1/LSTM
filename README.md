# 🚀 Tesla Stock Price Forecasting using LSTM Neural Networks

This project is a deep learning-based time series forecasting model developed to predict the **future stock prices of Tesla (TSLA)**. Using **Long Short-Term Memory (LSTM)** networks — a special kind of recurrent neural network well-suited for sequential data — we aim to capture the underlying patterns and trends from Tesla's historical stock data.

This project is part of an academic initiative in the **Big Data Analytics PGDM program at FORE School of Management**, intended to demonstrate practical knowledge of deep learning in financial forecasting.

---

## 🔎 Objective

The goal of this project is to build a predictive model that:
- Learns temporal dependencies in Tesla's stock price history,
- Forecasts future closing prices based on past trends,
- Helps identify the feasibility and challenges of using LSTM for real-world stock prediction.

Unlike traditional models that rely on linear regression or ARIMA, this approach uses a deep learning framework that can potentially uncover non-linear and long-term dependencies.

---

## 🗂️ Project Components

Here’s a breakdown of the files and notebooks in this repository:

- `archive (4).zip`: Contains raw Tesla stock price historical data in CSV format.
- `DLM_LSTM.ipynb`: The core model implementation — data preparation, feature scaling, LSTM design, training, and evaluation.
- `LSTM_REPORT.ipynb`: A complete report notebook explaining the project flow in a clean, reader-friendly format.
- `tesla_predictions.csv`: Output file storing the model's predictions for visualization and further analysis.

---

## 📊 Dataset Overview

The dataset contains several years of **Tesla Inc. (TSLA)** stock trading data, sourced likely from Yahoo Finance or a similar platform. It includes the following attributes:

- `Date`: Trading date
- `Open`: Opening price of the day
- `High`: Highest price of the day
- `Low`: Lowest price of the day
- `Close`: Closing price of the day (used as target variable)
- `Volume`: Number of shares traded

We use the `Close` price for forecasting, assuming it's the most representative of the stock's value at a given time.

---

## 🧪 Exploratory Data Analysis (EDA)

Before modeling, extensive EDA was performed to:
- Identify trends, volatility, and price movements over time,
- Check for missing values or outliers,
- Normalize the data for stable LSTM learning.

Visual tools like line plots and moving averages were used to explore patterns, volatility, and correlations.

---

## 🧠 Model Architecture

The LSTM model used here consists of:

- **Input Layer**: Historical `Close` prices in sequences (windowed time steps).
- **Two LSTM Layers**: With dropout regularization to prevent overfitting.
- **Dense Layer**: Outputs a single prediction (next closing price).
- **Activation**: ReLU for intermediate layers, linear for the final output.

We trained the model on 80% of the dataset and validated it on the remaining 20%.

> LSTM is particularly useful here as it can remember long-term dependencies, unlike standard RNNs.

---

## 📈 Model Performance & Visualization

The performance was measured using:
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**

Key visualizations:
- Predicted vs Actual prices
- Loss curves across epochs
- Zoomed-in views of key trends (e.g., post-COVID surge)

> The model shows promising results with a clear overlap between the actual and predicted curves in validation.

---

