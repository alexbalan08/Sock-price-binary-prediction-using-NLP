# 📈 Personal NLP Project: Predicting Stock Price Movements Based on News

This project explores the use of Natural Language Processing (NLP) techniques to **predict stock price movements** based on news reports, focusing on the **car manufacturing sector**. Multiple transformer-based models (decoders only) were applied to both company-specific and multi-company datasets, using time-lagged stock price data to analyze the impact of news on financial performance.

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
- Stop word removal (notnecessary for Transformers models however. I stronlgy advice to try the work using the full corpuses)
- No stemming or lemmatization (to preserve context, again not really needed for transformers with short sentences)
- Multiple **time windows** analyzed:
  - Stock price movement **1 day**, **3 days**, and **5 days** after news release

---

## Models Used

All models were sourced from [Hugging Face](https://huggingface.co):

-As this is a **classification task**, a decoder model will alaways produce better results than other arhitectures. No need to try GPT models for example. 

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
   - Basic text cleaning (no aggressive normalization)
3. **Model Implementation**
   - Applied transformer-based classification models from Hugging Face
4. **Evaluation**
   - Performance compared across timeframes and model architectures

---

## Notes

- This is a **testing-focused NLP research project**, so results may vary from initial baselines.
- Models were not tuned for production performance but for exploring relative effectiveness on financial sentiment prediction.

---

The notebook presents detailed results with explanantions and steps. 
