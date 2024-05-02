# Fin-news-sentiment-analysis

# Overview

This repo explores the financial news dataset from Hugging face. The dataset has a collection of 4840 sentences and the sentiment of each sentence. The selected collection of phrases was annotated by 16 people with adequate background knowledge on financial markets.Given the large number of overlapping annotations (5 to 8 annotations per sentence), there are several ways to define a majority vote based gold standard. To provide an objective comparison, 4 alternative reference datasets was provided based on the strength of majority agreement

- sentences with 100% agreement 
- sentences with more than 75% agreement
- sentences with more than 66% agreement 
- sentences with more than 50% agreement

# Business Understanding

This project aims to develp a Machine learning model using machine readable text to analyse the sentiment of a financial news. Techiniques like stemming, lemmatization, Count Vectorizer and Tfid Vectorizer will be used to pre-process the text data. Models using algorithms like logistic regression, decision trees, and bayes will be developed to identify the best performing model to classify a news as positive, negative or neutral. The models developed will help financial advisors, analysts to understand health and trend of financial services.

# Data Understanding & Preparation

- No missing data
- Decided to use the data with 100% agreement. This subset of the data had 2264 news data
- Each news is classified as positive, negative or neutral
- The proportion of the sentiment: Positve 25.18%, negative-13.38% & neutral-61.44%
- There were more news with length around 90 to 99 characters and in general between 40 and 250 characters
- The number of words seems to vary from 5 to 50
- Top 10 stop words are "the', "of", "in","and","to","a","for","from","is","will"
- Most common non-stop words are "eur","mn","company","profit","net","million","sales","finnish","said","operating"
- Noticed words like "net profit" , "increased" in the positive sentiment and words like "net loss" and "decreased" in negative sentiment
- The word "Finnish" appear in all sentiments which makes me think most of these news in the data are collected from Finland
- Used stemmer techinique to process the words to it root form
- Used lemmatization techinique which stems the words based on context
- Decided to use the lemmatized content to build the model since we are dealing with financial news
- Used Count Vectorizer and Tfid Vectorizer to convert the text date into a sparse matrix

# Modeling

Built two logistic regression models ,one using the pre-processed data using Count Vectorizer and the other using Tfid Vectorizer.The Logistic regression model with Count Ventorizer has better accuracy than Tfid Vectorizer. I expected the model with Tfid Vectorizer to perform better because it focuses on the importance of words in the text. So there is scope to tune this model. Will expore it in part 2 of the capstone

![image](https://github.com/manikrajan/Fin-news-sentiment-analysis/assets/6862254/104c6018-d8cd-4ca3-98e3-2f5bca5683fd)

