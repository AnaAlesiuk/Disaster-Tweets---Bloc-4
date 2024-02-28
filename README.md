# Disaster-Tweets---Bloc-4

my email: anastasia@phiskills.com

video-explanation: https://youtu.be/BLQ-ZRTOnZ4


## Goal

In this project, the goal was to predict whether a given tweet was about a real disaster or not. If so, predict a 1. If not, predict a 0.

## Text cleaning

After looking at the given data, we can see a lot of punctuation, URL signs, hashtags, stop words, and so on. So, the first step in our work will be text cleaning. But before doing this, I decided to merge two datasets to make it easier to clean the entire area. I also used the spaCy library for NLP. With the help of it, I can detect all the stop words (the ones that do not add any value to a sentence). 
Returning to text cleaning, it includes case normalization (every word is in the same case, and the computer doesn’t process the same word as two different tokens), removing URLs, HTML tags, punctuation and stop words. Also, during text cleaning, I used lemmatization to help transform words into their actual root. 

## Train_test_split

The next step was to split our data frame into train, test and target. Train - what we will show our Machine Learning model, target - what prediction it is supposed to have and test - what we will give a model at the end to see how well it predicts our tweets.

## Text vectorization

The word embeddings of our dataset can be learned while training a neural network on the classification problem. Before it can be presented to the network, the text data is encoded so that a unique integer represents each word. So, I tokenized my train, validation and test.

## Embedding Matrix

Embedding is a way to extract the meaning of a word. In the embedding process, each word (or more precisely, each integer corresponding to a word) is translated to a vector in N-dimensional space. 
I downloaded pre-trained word vectors from GloVe to create a word embedding matrix. And then created an embedding matrix that maps each word index to its corresponding embedding vector

## Model

Here I created a Sequential keras model that contains an Embedding layer with an embedding matrix as initial weight, a dropout layer to avoid over-fitting, an LSTM layer that includes long-short term memory cells and an activation layer - sigmoid as value for sigmoid function lies between 0 and 1 only.

## Results

As we can see, the accuracy and loss scores look good.
