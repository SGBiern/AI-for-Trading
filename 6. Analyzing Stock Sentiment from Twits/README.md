# Sentiment Analysis with Recurrent Neural Network (RNN) from Twits

This project contains

  1. Loading Twits data and preprocessing: 
  
    1) cleaning (removing URLs, ticker symbols, StockTwits and non-letter)
    2) lemmatizing
    3) excluding very high and low frequently appearing words
    4) tokenizing
    5) balancing sentiments
 
  2. Constructing a RNN (embedding -> RNN -> fully connected layer -> log-softmax activation) 
  
    1) loading pre-trained embedding vectors: glove.6B.100d.txt from [GloVe](https://nlp.stanford.edu/projects/glove/)
    2) implementing GRU as RNN
    3) yielding sentiment probability from fully connected layer
  
 The dataset is from the social media site [StockTwits](https://en.wikipedia.org/wiki/StockTwits).
 
 # Requirements
 
  * json >= 2.0.9
  * nltk >= 3.2.5
  * torch >= 0.4.0
  * numpy >= 1.12.1
  * pandas >= 0.23.3
  * tqdm == 4.19.5
  
 # How to run
 
Please execute all the command lines in sentiment_analysis_RNN_from_twits.ipynb, where results are.

# Experiment results

The best accuracy is _73.3%_, when implementing the better options in the follwoing experiements.

1. Regarding preprocessing
  * Keeping stopwords performs better than removing them.
  * Lemmatizing to current tone performs better.
  * Sequency length of 25-35 performs the best (the largest length of a token is 40.)
  * Excluding too many high and low frequency words performs poorly.
  
2. Regarding Network
  * LSTM and GRU both perform similarly, however GRU trains faster.
  * Pre-trained embedding does not lead to significant performance difference, compared to using non-pre-trained embedding whose dimension is 300-400.
  * batch normalization leads to no performance difference.
  * Uni-directional RNN with 2 layers performs better than Bi-directional RNN with 2 layers.

