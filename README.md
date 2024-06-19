# Stock-sentimental-analysis
# Trading Strategy Based on News Sentiment Analysis

## Overview
This project implements a trading strategy based on sentiment analysis of news headlines for Meta Platforms, Inc. (META). It uses a Random Forest classifier to predict market sentiment from news headlines and generates trading signals (buy/sell) accordingly. The performance of this strategy is evaluated using several financial metrics.

## Data
- **News Headlines Dataset (`headlines.csv`):** Contains news headlines with corresponding dates and labels indicating market sentiment.
- **Stock Data:** Historical stock data for META fetched using `yfinance`.

## Steps
### 1. Data Preparation and Sentiment Analysis
- **Load Data:** Read news headlines data from `headlines.csv`.
- **Data Splitting:** Split the data into training and test sets based on the date.
- **Data Preprocessing:** Clean and preprocess the training headlines by converting text to lowercase and removing non-alphabetical characters.
- **Text Vectorization:** Combine headlines into a single string per day and use `CountVectorizer` to create bigrams.
- **Model Training:** Train a Random Forest classifier on the vectorized headlines.
- **Sentiment Prediction:** Predict sentiments for the test set headlines.
- **Model Evaluation:** Evaluate the model's performance using confusion matrix, accuracy score, and classification report.

### 2. Stock Data and Signal Generation
- **Fetch Stock Data:** Retrieve historical stock data for META from March 1, 2000, to January 7, 2016, using `yfinance`.
- **Merge Data:** Merge the sentiment predictions with the stock data on the date.
- **Generate Trading Signals:** Generate buy signals for positive sentiment and sell signals for negative sentiment.

### 3. Simulate Trading Strategy
- **Initialize Portfolio:** Start with an initial cash of $10,000.
- **Execute Trades:** Execute buy/sell trades based on generated signals and track the portfolio value over time.

### 4. Performance Metrics
- **Sharpe Ratio:** Measures the risk-adjusted return of the portfolio.
- **Maximum Drawdown:** Measures the maximum observed loss from a peak to a trough of the portfolio value.
- **Number of Trades Executed:** Total number of buy and sell trades executed.
- **Win Ratio:** Proportion of trades that were profitable.

## Results
- **Initial Cash:** $10,000
- **Final Portfolio Value:** $11,903.55
- **Total Return:** 19.04%
- **Sharpe Ratio:** Calculated from portfolio returns.
- **Maximum Drawdown:** Calculated from portfolio value series.
- **Number of Trades:** Counted from signal generation.
- **Win Ratio:** Proportion of profitable trades.

## Usage
1. **Clone the Repository:**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
