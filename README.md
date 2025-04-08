#Predictive Analysis of NVIDIA Stock Prices Using Machine Learning"

### Project description

The primary goal of this project is to analyze historical stock price data of NVIDIA Corporation and build predictive machine learning models to forecast future closing prices, leveraging time-based features and trend patterns.

###  Objectives:

1) Understand and explore the structure and content of NVIDIA’s historical stock price dataset.

2) Clean and preprocess the data to make it suitable for analysis and modeling.

3) Perform exploratory data analysis (EDA) to gain insights into price trends, volatility, and feature relationships using visualization techniques.

4) Engineer relevant features, such as lag variables and moving averages, to capture temporal patterns in the stock data.

5) Train and evaluate regression models (e.g., Linear Regression and Random Forest Regressor) to predict future stock prices.

6) Compare model performance using evaluation metrics like Mean Squared Error (MSE), Mean Absolute Error (MAE), and R² Score.

7) Interpret and visualize model results, including prediction vs. actual performance, to assess accuracy and usefulness.
   

### Dataset Summary:

The dataset (NVIDIA_STOCK.csv) contains daily historical stock price data for NVIDIA Corporation, including:

- Date: The trading date.

- Open, High, Low, Close, Adj Close: Price information for each day.

- Volume: Number of shares traded on that day.

  

  ### Key Insights from Visualizations:
  
- The stock price trend shows substantial growth over time, especially post-2020.

-Moving averages helped smooth out volatility and reveal underlying trends.

-Correlation analysis highlighted strong relationships between features like Open, High, Low, and Close prices.

-Model performance visualization showed that Linear Regression significantly outperformed Random Forest, as seen by its higher R² and closer alignment with actual prices.

### Machine Learning Implementation

## Model Setup:

To predict the daily closing price of NVIDIA stock, we treated this as a regression problem, since the target variable (Close) is continuous. We used the following models:

1) Linear Regression

2) Random Forest Regressor
   

### Data Preparation:

-Features (X): Lagged values of Adj Close, Close, High, Low, Open, and Volume from previous days.

-Target (y): Today's Close price.

- Data was split into training (80%) and testing (20%) sets, with no shuffling to preserve time sequence.

### Model Results:

Model	             MSE	    MAE    	R² Score
-Linear Regression	~7.90  	 Low	      0.99
-Random Forest 	2664.38	   40.82	    -1.67

### Interpretation:

1) Linear Regression performed extremely well, capturing the stock price patterns with high accuracy.

2) Random Forest surprisingly underperformed. This may be due to its inability to generalize time-series trends as effectively without sequence-based tuning.










