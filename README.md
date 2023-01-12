# NLP_Sentiment_Identification

This project is submitted as python implementation in the contest of Analytics Vidhya called "Identify the Sentiments". I enjoyed learning and experiemting with new domain in data science. So, this is my first project in NLP.

The contest URL: https://datahack.analyticsvidhya.com/contest/linguipedia-codefest-natural-language-processing-1/

Problem Statement
Sentiment analysis remains one of the key problems that has seen extensive application of natural language processing. This time around, given the tweets from customers about various tech firms who manufacture and sell mobiles, computers, laptops, etc, the task is to identify if the tweets have a negative sentiment towards such companies or products.

_Dataset_
1)The train set contains 7,920 tweets
2)The test set contains 1,953 tweets

**Implementation Approach**

Text Cleaning and Preprocessing

A) We applied the below text preposessing on the training and testing tweets sets:
1.URLs removal: We have used Regular Expressions (or RegEx) to remove the URLs.
2.Punctuation marks removal: remove any punction marks from the text.
3. Numbers removal: replace any digits in the tweets with space.
4. Whitespaces removal
5. Convert the text to lowercase.


B) Text normalization by reducing the words to its base form by using the spacy library.

C) Tweets to ElMo Vectors

We imported and used the pretrained ELMo model from the Tensorflow Hub, where we extracted ELMo vectors for the cleaned tweets in the train and test datasets. Each tweet is represented by an ELMo vector of length 1024 interms of the tweet's words/tokens.

D) Tweets to BERT Vectors

We imported and used the pretrained google BERT model, where we extracted BERT vectors for the cleaned tweets in the train and test datasets. Each tweet is represented by an BERT vector of length 768 interms of the tweet's words/tokens.

Model Building

D) Classifiaction Model Building and Evaluation
We have used the ELMo vectors and BERT vecyors as features of the train dataset to build and train a classification model. We evaluated our model by the F1 score metric since this is the official evaluation metric of the contest. We train a logistice model and get **F1 socre of 0.88**
