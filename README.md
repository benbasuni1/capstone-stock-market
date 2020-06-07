# Springboard Capstone: Predicting the Stock Market

# The Data
We will be using a subset of the NYSE/SEC DataSet obtained from Kaggle:   
https://www.kaggle.com/qks1lver/amex-nyse-nasdaq-stock-histories?    
https://www.kaggle.com/finnhub/reported-financials     

Finnhub gives access to realtime market data from stock exchanges, 10 forex brokers and 15+ crypto exchanges.
They also provide institutional-grade alternative and fundamental data for global companies through their stock API. Finnhub is ranked number 1 on Towards Data Science stock API guide. With the sole mission of democratizing financial data, Finnhub offers a free realtime API for stocks, forex and cryptocurrency. 

# Our Goal
The problem this capstone project aims at solving is predicting whether or not a Fortune 500 company will still be on the list in the next year year. By analyzing financial statements of companies, this project aims at coming up with a model that could accurately guess whether or not a company would still be in the top 500 companies the next year. 

Our aim is to find patterns to see whether or not we can determine a company's valuation and assess whether or not they are likely to go up in stock prices. 

# Data Overview
There are many Stock Exchange data sets on Kaggle. We will be using 2 datasets. They both combined with about 2GB of data.

# Approach
The problem was divided into several steps:

1. **Data Wrangling (Pre-Production):** Before even uploading the datasets onto Kaggle or in a Jupyter Notebook, I had to first wrangle with the JSON data that was provided by Finnhub. The data could not be strictly imported using Pandas with `pd.read_json`. The data wrangling logic can be found in `handle-sec-data.js`.
2. **Data Wrangling in Kaggle:** The datasets were uploaded inside of a Jupyter notebook and explored. Missing and polluted values were discarded and filled in wherever appropriate.
3. **Exploratory Data Analysis:** Extensive data visualization and summary statistics were used to extract insights and pattern from the data.
5. **Feature Engineering:** From the insights discovered in the previous step, new features were engineered and redundant features were dropped. A few variables were binned in order to give greater accuracy.
6. **Machine Learning:** Various classifiers were tested and their accuracy recorded. The best classifier was then hyperparameter tuned using Grid Search Cross Validation. This model was then fit on the test users and the final submission file was obtained.

**Final Results**

**Repository Structure**
