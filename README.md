# Natural Language Processing - TensorFlow 2.0 

[![Tensorflow](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT7b9ZDD7lMdkByT-f_RCAqSQYqnq_CpgD16IFrwfmUwWCmdt7H)](https://colab.research.google.com/github/JohnAntonusMaximus/natural-language-processing-tensorflow/blob/master/Recurrent_Neural_Network_TensorFlow_2_0.ipynb\)

[![Colab](https://camo.githubusercontent.com/52feade06f2fecbf006889a904d221e6a730c194/68747470733a2f2f636f6c61622e72657365617263682e676f6f676c652e636f6d2f6173736574732f636f6c61622d62616467652e737667)](https://colab.research.google.com/github/JohnAntonusMaximus/natural-language-processing-tensorflow/blob/master/Recurrent_Neural_Network_TensorFlow_2_0.ipynb\)

## Background

This dataset contains movie reviews along with their associated binary sentiment polarity labels. It is intended to serve as a benchmark for sentiment classification. This document outlines how the dataset was gathered, and how to use the files provided.

The core dataset contains 50,000 reviews split evenly into 25k train and 25k test sets. The overall distribution of labels is balanced (25k pos and 25k neg). We also include an additional 50,000 unlabeled documents for unsupervised learning.

In the entire collection, no more than 30 reviews are allowed for any given movie because reviews for the same movie tend to have correlated ratings. Further, the train and test sets contain a disjoint set of movies, so no significant performance is obtained by memorizing movie-unique terms and their associated with observed labels. In the labeled train/test sets, a negative review has a score <= 4 out of 10, and a positive review has a score >= 7 out of 10. Thus reviews with more neutral ratings are not included in the train/test sets. In the unsupervised set, reviews of any rating are included and there are an even number of reviews > 5 and <= 5.

The original dataset can be found here:
https://www.kaggle.com/iarunava/imdb-movie-reviews-dataset


## Labels (Object Classes)

This model uses binary classification to determine if a review is positive or negative. If the probability of the output function is greater than 0.5, the review is positive, if its less, than the review is negative.
									



## Approach

In this model, I used a recurrent neural network using an embedding layer and an LSTM layer for text classification. Preprocessing through the tf.kears.preprocessing module was using to pad each of the word sequences to 100 for each review. 

On the training set, I was able to achieve aabout an 86% accuracy, and a little less on the test set using only 5 epochs. More training or dropout could be added to improve results.  


# Links

* [KaizenTek](http://www.kaizentek.io) - IT Consulting & Cloud Professional Services  
