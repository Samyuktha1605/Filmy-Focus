# Filmy-Focus

ABSTRACT :

Movie review rating has become a huge demand for the current era due to the rapid growth of the movie industry. Sentiment Analysis  has been applied to determine the sentiment conveyed by people in various situations. For instance, it can be useful for recommender systems, which may exploit the sentiment expressed by a user and predict their sentiment regarding the topic, and recommend those for which a positive sentiment is predicted. One particular application centers on the use of the sentiment conveyed by the words, as features for predicting the scores of movies and movie reviews.

We are interested in knowing whether movie reviews are positive or negative, which companies and individuals use the sentiment analysis in a variety of settings, particularly for marketing purposes. 


WORKING :

The Dataset

Our data source is a 40,000 row dataset with 2 columns- Review, is in a series of strings written by movie reviewers ; Label, either positive or negative, is the sentiment set by a human based on the movie review. 


Preprocessing

Basic pre-processing for text consists of:
Removing non-alphabetic characters and stop words
Changing all words to lowercase
Removal of extra tags like < br >< br >, other links and special characters.
Tokenization of review into words.
Lemmatization of each word.

Representation of text as vector

We then use Word2vec (Word to Vector) which is a two-layer neural net that processes text. Its input is a text corpus and its output is a set of vectors: feature vectors for words in that corpus. It is better at learning words in their surrounding context. The purpose and usefulness of Word2vec is to group the vectors of similar words together in vector space, as it considers the semantic meaning of words. 

Classifier

For this classification we will use sklean’s Multi-Layer Perceptron classifier (MLP).

Our aim is to improve the model in any way possible. One important factor in the performance of the model is its hyperparameters. Once we set appropriate values for the hyperparameters, the performance of the model can improve significantly. GridSearchCV, a function that comes in Scikit-learn, is the process of performing hyperparameter tuning in order to determine the optimal values for a given model. GridSearchCV tries all the combinations of the values passed in the dictionary and evaluates the model for each combination using the cross-validation method. Hence after using this function we get accuracy / loss for every combination of hyperparameters and we can choose the one with the best performance.

The hyperparameters we wish to tune are: 
No. of hidden layers
Size of each hidden layer
Activation function in hidden layer
Learning rate


RESULTS :

Finally to evaluate the performance of our model, we use various metrics. The model exhibits:
Accuracy : 0.85
Precision: 0.82
Recall   : 0.90
f1_score : 0.86

