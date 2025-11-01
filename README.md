# AIML STOCK PREDICTION MODEL

This is a Python-based project that analyzes and predicts stock prices. You can choose a company like Apple or Tesla, and the program will show you two things:
1.  A graph of the stock's past performance with 🟢 **Buy** and 🔴 **Sell** signals based on a common trading strategy.
2.  An AI-powered 7-day forecast of where the price might go next.

The entire project runs in a single Google Colab notebook.

## PREVIEW

### GRAPH 1: HISTORICAL ANALYSIS WITH SMA & TRADING SIGNALS
<img width="1151" height="624" alt="image" src="https://github.com/user-attachments/assets/05ad568f-58c4-4ef8-95b0-a4e93bda199e" />

### GRAPH 2: 7-DAY AI-POWERED PRICE FORECAST
<img width="1151" height="624" alt="image" src="https://github.com/user-attachments/assets/95da26a0-0a29-4803-9d46-299828d2587b" />

## FEATURES

* **USER-FRIENDLY MENU:** Select from 10 major companies (like Apple, Google, Tesla) to analyze.
* **TECHNICAL ANALYSIS:** Automatically calculates the 9-period Simple Moving Average (SMA) from 1 year of historical data.
* **TRADING SIGNALS:** Plots clear **Buy** 🟢 and **Sell** 🔴 signals on the chart based on price-SMA crossovers.
* **AI-POWERED FORECASTING:** Uses a Long Short-Term Memory (LSTM) neural network to predict the stock price for the next 7 days.
* **CLEAR VISUALIZATIONS:** Generates two plots:
    1.  The complete 1-year price history with SMA and trading signals.
    2.  A focused 7-day forecast showing the predicted trend.

## HOW IT WORKS

The project is divided into two main parts:

### 1. TECHNICAL ANALYSIS (SMA SIGNALS)
The notebook first fetches 1 year of historical data for the user-selected stock. It then calculates a **9-day Simple Moving Average (SMA)**, which is a lagging indicator that helps smooth out price data to show the trend.
* A **"Buy" signal** 🟢 is generated when the stock's closing price crosses *above* the blue SMA line.
* A **"Sell" signal** 🔴 is generated when the stock's closing price crosses *below* the blue SMA line.

### 2. PREDICTIVE MODEL (LSTM FORECAST)
To predict future prices, the project uses a **Long Short-Term Memory (LSTM)** model, a type of Recurrent Neural Network (RNN) perfect for time-series data.
1.  **PREPARE DATA:** The model is trained on the last year of closing prices, looking at 60-day sequences to learn patterns.
2.  **TRAIN MODEL:** The LSTM network is built and trained in TensorFlow/Keras to understand the stock's complex patterns.
3.  **PREDICT:** The model uses the last 60 days of known data to predict the next 7 days, one day at a time.

## TECHNOLOGIES USED

* Python
* Google Colab
* yfinance
* Pandas
* NumPy
* TensorFlow / Keras
* Matplotlib
* Scikit-learn

## HOW TO RUN

1.  Open the `.ipynb` file in **Google Colab**.
2.  Run the **first (and only) code cell**.
3.  The program will first install all necessary libraries.
4.  A menu will appear in the output. **Type the name** of the company you want to analyze (e.g., tesla) and press **Enter**.
5.  The script will run from start to finish, outputting the data, the two graphs, and the final 7-day price predictions.

## TEAM MEMBERS

* **S Subash:** TEAM LEAD
* **PREM B SULE:** Stock Analysis Expert
* **ZABI MOHAMMED:** Documentation and Reporting
* **NISARG SHETTAR:** Quality Assurance and Testing
