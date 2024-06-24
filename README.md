# GARCHvsLSTM

# Portfolio Volatility Forecasting

This repository contains the code and data used in the study of portfolio volatility forecasting using GARCH-family models and Long Short-Term Memory (LSTM) neural networks. The primary goal of this study is to compare the performance of traditional econometric models with deep learning techniques in predicting financial market volatility.

## Table of Contents
1. [Introduction](#introduction)
2. [Data](#data)
3. [Models](#models)
   - [GARCH-family Models](#garch-family-models)
   - [LSTM Model](#lstm-model)
4. [Results](#results)
5. [Conclusion](#conclusion)
6. [Usage](#usage)
7. [References](#references)

## Introduction
Volatility forecasting is crucial for risk management, derivative pricing, and financial decision-making. This project implements and evaluates several volatility forecasting models, including GARCH(1,1), GARCH-t, EGARCH, TGARCH, and an LSTM neural network. The performance of these models is compared using metrics such as Mean Absolute Error (MAE) and Mean Squared Error (MSE).

## Data
The dataset used in this study consists of daily returns of a financial portfolio. The data spans from January 2000 to December 2023 and includes features such as:
- Portfolio returns
- Exponential moving averages
- Rolling volatility
- Technical indicators (Bollinger Bands, RSI, MACD, ROC)

## Models

### GARCH-family Models
GARCH-family models are widely used for volatility forecasting due to their ability to capture time-varying volatility and leverage effects. The following models are implemented:
- **GARCH(1,1)**: Basic Generalized Autoregressive Conditional Heteroskedasticity model.
- **GARCH-t**: GARCH model with Student's t-distribution.
- **EGARCH**: Exponential GARCH model that captures asymmetries in volatility.
- **TGARCH**: Threshold GARCH model that allows different responses to positive and negative shocks.

### LSTM Model
LSTM neural networks are a type of recurrent neural network (RNN) capable of learning long-term dependencies. They are well-suited for time series forecasting tasks. The LSTM model in this study consists of:
- Two LSTM layers with 100 and 50 units, respectively.
- Dropout layers to prevent overfitting.
- A dense output layer for volatility prediction.

## Results
The models' performance is evaluated using out-of-sample predictions. The Diebold-Mariano (DM) test is used to statistically compare the predictive accuracy of the models. Key findings include:
- EGARCH outperforms other GARCH-family models in terms of MAE and MSE.
- The LSTM model demonstrates superior performance compared to GARCH-family models, especially in capturing non-linear dependencies.

## Conclusion
The study concludes that while GARCH-family models are effective for volatility forecasting, LSTM neural networks provide better accuracy and handle non-linear dependencies more effectively. These findings have significant implications for financial modeling and risk management.

## Usage
To reproduce the results, follow these steps:
1. Clone this repository: `git clone https://github.com/yourusername/yourrepository`
2. Navigate to the project directory: `cd yourrepository`
3. Install the required packages: `pip install -r requirements.txt`
4. Run the data preprocessing script: `python preprocess_data.py`
5. Train and evaluate the models: `python train_models.py`
6. Generate the results and visualizations: `python generate_results.py`

## References
- Bollerslev, T. (1986). Generalized Autoregressive Conditional Heteroskedasticity. *Journal of Econometrics*, 31(3), 307-327.
- Hochreiter, S., & Schmidhuber, J. (1997). Long short-term memory. *Neural Computation*, 9(8), 1735-1780.
- Kim, K. J., & Won, C. H. (2018). Forecasting the volatility of stock price index: A hybrid model integrating GJR-GARCH and LSTM neural networks. *Expert Systems with Applications*, 103, 25-37.
- [Full list of references in the report]


