# NLP Project: Predicting Stock Price Movements Based on News - Bachelor Thesis

This project explores the use of Natural Language Processing (NLP) techniques to **predict stock price movements** based on news reports, focusing on the **car manufacturing sector**. Multiple transformer-based models (encoders only) were applied to both company-specific and multi-company datasets, using stock price data to analyze the impact of news on financial performance, after the release of the news 1 day, 3 days and 5 days later. 

> Labeled dataset I created available on Kaggle:  
> [Car Manufacturing Companies - News Reports](https://www.kaggle.com/datasets/alexbalan08/car-manufacturing-companies-related-newsreports)

---

## Dataset

- **Source**: News and financial data collected from [FactSet](https://www.factset.com)
- **Time Span**: 20 years
- **Companies Covered**: 30 car manufacturers (top 30 based on Market Cap in 2023)
- **Two dataset versions**:
  - **Multi-company dataset**: News for 30 companies
  - **Single-company dataset**: News for one specific company, same timeframe and preprocessing- Ford Motor Company (because I'm a Ford fan :) )

---

## Data Preprocessing

- Lowercasing
- Stop word removal (not necessary for Transformers models however, especially if the news are short. I stronlgy advice to try the work using the full corpuses)
- No stemming or lemmatization (to preserve context, again not really needed for transformers with short sentences)
- Multiple **time windows** analyzed:
  - Stock price movement **1 day**, **3 days**, and **5 days** after news release

---

## Models Used

All models were sourced from [Hugging Face](https://huggingface.co):

-As this is a **classification task**, an encoder model will alaways produce better results than other arhitectures (maybe nowdays with gpt-4...).  

- **BERT**
- **RoBERTa**
- **FinBERT** (financial-domain-specific transformer)
  

Each model was:
- Used in its **pre-trained** form
- Optionally **fine-tuned** on the collected dataset

---

## Project Workflow

1. **Data Collection**
   - News and stock price data from FactSet
2. **Preprocessing**
   - Basic text cleaning + stop words removal
3. **Model Implementation**
   - Applied transformer-based classification models from Hugging Face + fine tunning them on my dataset
4. **Evaluation**
   - Performance compared across timeframes and models on both datasets (30 companies and only Ford)

---



- A report with the findings and research case study is available as well.
  
---

The notebook presents detailed results with explanantions and steps. 
