## Stock_Movement_Analysis

## Overview
This project predicts stock movements based on sentiment analysis of Reddit posts and historical stock data. It combines data scraping, natural language processing (NLP), and machine learning to analyze and forecast stock price changes.

## Project Structure

### 1. Scraping Data from Reddit
- **Library Used**: `praw` (Python Reddit API Wrapper)
- Fetches posts related to the stock market from Reddit.
- Extracts titles, content, and other metadata.

### 2. Data Cleaning and Processing
- Removes noise from text data, including URLs, special characters, and unnecessary spaces.
- **Function Used**: `clean_text` for preprocessing textual data.

### 3. Sentiment Analysis
- Analyzes the sentiment of cleaned text using `TextBlob`.
- Computes sentiment polarity values (-1 for negative, 0 for neutral, 1 for positive sentiment).

### 4. Preparing Stock Movement Data
- **Library Used**: `yfinance` (Yahoo Finance API)
- Downloads historical stock data for selected tickers.
- Calculates daily percentage changes and creates a binary label for stock movements (1: upward, 0: downward).

### 5. Model Building
- **Algorithm**: Random Forest Classifier (from `sklearn`).
- Features include sentiment polarity, and the target variable is stock movement.
- Splits data into training and testing sets.

### 6. Evaluation and Visualization
- Evaluates the model's performance using metrics like accuracy, confusion matrix, and classification report.
- Visualizes the confusion matrix using `seaborn`.

## Getting Started

### Prerequisites
- Python 3.7+
- Install dependencies using the following command:
  ```bash
  pip install -r requirements.txt
  ```

### Dependencies
- `pandas`
- `numpy`
- `praw`
- `textblob`
- `yfinance`
- `sklearn`
- `matplotlib`
- `seaborn`

### Running the Project
1. Clone the repository:
   ```bash
   git clone <https://github.com/Rajitha56/Stock_Movement_Analysis.git>
   cd <Stock_Movemen_Analysis>
   ```

## File Details
- **`Stock_Movement_Analysis.ipynb`**: Main notebook containing all steps from data scraping to evaluation.
- **`data.csv`**:Contains the scraped Reddit data
- **`scraping.ipynb`**:Notebook for scraping Reddit data
- **`preprocess&modelling`**:Notebook for data cleaning, sentiment analysis, and model building.
- **`requirements.txt`**: List of required Python libraries and versions.

## Results
- Provides insights into stock price changes based on sentiment analysis.
- Demonstrates the correlation between Reddit sentiments and stock movements.


