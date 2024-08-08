# Personal NLP Project: Predicting Stock Price Movements Based on News

**Note:** Testing has been done, and code and results might differ from the baseline.


Predicting stock price movements based on news, focusing on a specific business sector- car manufacteering
Data collected over a time frame of 20 year for 30 companies
Stop words and lower case removal. no need for stemming or lemmatization 
2 different datasets, one containing 30 companies (larger dataset) and a smaller dataset containing news of a single company (same time frame of time, same pre processing)
Different time frames for data were created, checking the influence of the news on the stock price 1 day, 3 days and 5 days, after the news release
1 day time frame datasets will be uploaded here
Different available open source models tested, including finBERT (specific for financial datasets). all models made available by https://huggingface.co


Main Steps:
-Fiancial data and news colected from FactSets.com (https://www.factset.com)
-Data cleaned and pre processed
-Impleemntation of BERT, roBERTa and finBERT (pre trained and fine tuned)
-Testing

