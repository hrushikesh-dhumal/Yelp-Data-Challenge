# Synopsis
The Yelp reviews are rich source of information for natural language processing applications. I am are building a sentiment analysis system for English language which analyzes how much of the review is positive or negative based on the text review and star rating Yelp Dataset Challenge. I use a combination of two feature generation methods and two machine learning models to find the best prediction result. My approach is to create bag of words from the top frequent words in all raw text reviews and using word embedding to create a high dimensional representation of each of the review. Then I do a performance measure of two machine learning algorithms- Support Vector Machines (SVM) and Long Short Term Memory (LSTM). I have used python to implement the system.

This repository has a sample data set to play around the code.

## [Data Cleaning](yelp_01dataCleaning.ipynb)
1.	Lowercase
2.	Remove numbers
3.	Remove stop words using nltk
4.	Porter Stemming
5.	Create sparse matrix representation using scikit.

## [Exploratory Data Analysis](yelp_02EDA.ipynb)
1.	Frequency vs Rank for a sample of yelp review dataset
2.	To find out the stop words we are using inverse term document frequency. 
3.	To create a baseline for evaluating the algorithm, we are plotted the distribution of star category ratings.
4.	To get a better intuition of the text data we plotted the most common and recurring words in each of the reviews.

## Analysis
1.	[Bag of Words Generation](yelp_03bagOfWords.ipynb) - [Bag of words](http://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.CountVectorizer.html) representation of the user reviews.
2.	[Word Embeddings](yelp_04word2vec)- [Word embeddings](https://radimrehurek.com/gensim/models/word2vec.html) representation of the user reviews.
3.	Create models to predict sentiments based on user review and rating
	
	1. [Support Vector Machine](yelp_06SVM.ipynb)
	
	2. [Long Short Term Memory Neural Network](yelp_06LSTM.ipynb)


# Installation
1. Clone the repository

	```
	git clone https://github.com/hrushikesh-dhumal/Yelp-Data-Challlenge.git
	```

2. Dependencies

Install the requirements using `pip install -r requirements.txt`

It is suggested that you have [Anaconda](https://www.continuum.io/downloads) which covers majority of the dependencies. 

## Execution instructions
Execute the playbooks in order of their serial number. 

The data cleaning has already been done in the sample data. In case you want work on entire data acquired from [yelp](https://www.yelp.com/dataset_challenge) create a directory named raw in data folder and download the data here. Then you will be able to execute the code in [yelp_01dataCleaning.ipynb](yelp_01dataCleaning.ipynb) notebook which will genrate csv which can be used in further analysis. 

	Note: if you want to use your own directory structure please edit the YELP_DATA_ in yelp_utils file


# Author Information
Hrushikesh Dhumal(hrushikesh.dhumal@gmail.com)
