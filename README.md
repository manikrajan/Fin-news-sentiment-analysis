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

Built 12 models (logistic regression, decision tree and Bayes) , using the pre-processed data with stemmed data & lemmatized data and using Count Vectorizer & Tfid Vectorizer.The Logistic regression model with stemmed data and Count Ventorizer has better accuracy(90%) than all the other models. Bayes models were much faster to fit but their accuracy was low compared to other models.Create a CNN model with Embedding layer,convolution layer, Max pooling layer,Dense layer,drop out layer and the output layer with sigmoid activation function. Plotting the losses , it seemed the model was overfitting. Applied early stopping to the model which resulted in an accuracy of 91% which was better than the logistic regression

![image](https://github.com/manikrajan/Fin-news-sentiment-analysis/assets/6862254/177463b4-e08b-4cb6-973e-e45e8a66bc4f)

# Evaluation

- The logistic regression model with stemmed data and Count vectorizer performed better than the other models.
- The CNN model had better accuracy than the Logistic regression model but it seems to overfit.
- The data had 2264 news entries. The overfitting in the CNN model could be avoided if we had more data.


