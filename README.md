# Twitter Sentimental Analysis 
![Twitter-arama](https://github.com/Kellyajara/Project_4/assets/127794801/3266f995-e0f2-4413-a9c8-764419719b8e)


By: Kelly Jara

## Overview
This project analyzes a dataset with curated tweets on google and apple products. In the dataset we have user tweets alongside with the products they are tweeting about and whether or not their tweet is depicting positive or negative emotions. Using this data, we were able to use NLP (Natural Language Processing) techniques to create a classification model that is able to predict whether a tweet has a positive or negative sentiment. 

Positive Tweet WordCloud:

![pos_wordcloud](https://github.com/Kellyajara/Project_4/assets/127794801/b0276ae0-cf90-4be7-ab4b-0fb9637fe60c)

Negative Tweet WordCloud:

![neg_wordcloud](https://github.com/Kellyajara/Project_4/assets/127794801/3e1744b1-ff7c-4c26-a363-4673855c9ff9)


## Business Problem
An emerging tech company is looking to get an idea of what consumers are saying about other companies, like Google and Apple, to see where they can look to improve their future models in order to compare to these top sellers. How can we analyze tweets about our products and determine if they are negative or positive? Can this help build rapport with our consumers and give us insight into how we can better our future models/services?

## Data
In this dataset we have over 9,000 tweets about tech products and whether or not the tweet was considered to have no emotion, positive emotion or negative emotion. 

Source: https://data.world/crowdflower/brands-and-product-emotions


## Preprocessing and Modeling
  Performed basic EDA steps in cleaning the data; removed the "product" column as it had a significant amount of NaN values and was mainly going to be looking at the sentiments of the tweets. Using a binary classification model, I had the target values as positive and negative emotion. I then conducted modeling using the CountVectorzer and TfidfVectorizer to see which yielded better results.
  To start off with modeling, I used a basic logistic regression to see how well the training sets performed and had a train score of 96%, test score of 88%. To continue testing out the datset, I then ran a Random Forest Classifier but found that my accuracy scores decressed and was only predicting accuarately 50% of the time. This occured becuase the dataset was significantly imbalanced, where we had a higher amount of positive tweets than negative tweets. 
  
![Screen Shot 2023-07-14 at 2 56 52 PM](https://github.com/Kellyajara/Project_4/assets/127794801/86d6c591-8c03-4f1c-9d63-eebe742c4806)
![Screen Shot 2023-07-14 at 3 00 41 PM](https://github.com/Kellyajara/Project_4/assets/127794801/016f8def-58aa-4657-9ce5-66689514c377)

Because the dataset was so imbalanced, the next best thing would be to run a Compliment Naive Bayes model. This type of model is great when working with imabalanced data as it calculates the probability of a tweet being either positive or negative rather than the probability of it belonging to one of those classes. When running the model, I found the scores to have increased, especially in terms of accuracy. 

![Screen Shot 2023-07-14 at 3 09 21 PM](https://github.com/Kellyajara/Project_4/assets/127794801/a9d53d02-ee97-46ec-b954-81f7f18724b7)
![Screen Shot 2023-07-14 at 3 09 31 PM](https://github.com/Kellyajara/Project_4/assets/127794801/da135601-013e-43a2-aada-8eea0c318a4c)

## Conclusion & Further Analysis
Based on the best model, it was able to have an accuracy score of 86% and and  train score of 96%. With this we are able to gather a large amount of tweets and be able to run them through the model to predict whether or not the sentiment behind the tweet is positve or negative. 

For future analysis:
- we can gather more data that has negative sentiment as it will balance our current data.
- Look at what product features are creating negative/positive feedback from consumers.
- What companies are people more likely to praise and how can those people be biased (are they soley apple users or android users).
- Create a new model with tweets that are outside of the tech scope for our model to get a better understanding of what words correlate with being positive or negative.
- Look into multiclassifiction. Out from positive and negative emotions, look at what is lacking in emotion. 
