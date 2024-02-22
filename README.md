# Text Classification Project

This project is a text classification task using the 20 Newsgroups dataset. The goal is to classify a given text into one of 20 categories.

## Table of Contents
1. [Dependencies](#dependencies)
2. [Dataset Description](#dataset-description)
3. [Data Preprocessing](#data-preprocessing)
4. [Model Training and Evaluation](#model-training-and-evaluation)
5. [Custom Implementation of Naive Bayes](#custom-implementation-of-naive-bayes)

## Dependencies
The project requires the following Python libraries:
- numpy
- pandas
- sklearn
- nltk


## Dataset Description
![image](https://github.com/javarath/TEXT-CLASSIFICATION-OWN-IMPLEMENTATION-VS-SKLEARN-IMPLEMENTATION-/assets/102171533/0a804b1e-6228-4262-97c7-3bffe4a894fc)
![image](https://github.com/javarath/TEXT-CLASSIFICATION-OWN-IMPLEMENTATION-VS-SKLEARN-IMPLEMENTATION-/assets/102171533/bf58c8c2-6463-465b-bca2-2cb28d38e062)

The 20 Newsgroups dataset is a collection of approximately 20,000 newsgroup documents, partitioned (nearly) evenly across 20 different newsgroups. The data is organized into 20 different newsgroups, each corresponding to a different topic. Some of the newsgroups are very closely related to each other (e.g. comp.sys.ibm.pc.hardware, comp.sys.mac.hardware), while others are highly unrelated (e.g misc.forsale, soc.religion.christian).

## Data Preprocessing
The data preprocessing involves several steps:

1. **Tokenization**: I split the text into individual words using the `tokenize` function.

2. **Stopword Removal**: I remove common words that do not contain important meaning. I use the nltk library's list of English stop words for this.

3. **Word Frequency Count**: I count the frequency of each word in the text. Words with a frequency greater than 80 are kept for the training set, and words with a frequency greater than 26 are kept for the test set.

The preprocessed data is then converted into a matrix of token counts (X for training data and XX for test data).

## Model Training and Evaluation
I use the Multinomial Naive Bayes model from sklearn. The model is trained on the training data and then used to predict the categories of the test data. The performance of the model is evaluated using a confusion matrix.

## Custom Implementation of Naive Bayes
In addition to using sklearn's implementation, I also implement my own version of the Naive Bayes algorithm. The custom implementation follows the same principles as the sklearn version. It calculates the log priors for each class and the log likelihoods for each word given a class. These values are then used to predict the categories of the test data. The performance of the custom implementation is also evaluated using a confusion matrix.
## Comparision of SKlearn vs Own Implementation:
**SKLEARN**
Class   Precision   Recall   F1-Score   Support
------------------------------------------------
0       0.33        0.60     0.43       199
1       0.51        0.50     0.50       242
2       0.19        0.02     0.03       263
3       0.47        0.55     0.50       262
4       0.50        0.54     0.52       234
5       0.63        0.60     0.62       230
6       0.60        0.62     0.61       257
7       0.56        0.56     0.56       265
8       0.51        0.65     0.57       251
9       0.35        0.66     0.46       226
10      0.45        0.22     0.29       262
11      0.61        0.59     0.60       257
12      0.44        0.49     0.46       229
13      0.71        0.56     0.63       249
14      0.72        0.47     0.57       256
15      0.62        0.65     0.63       243
16      0.57        0.62     0.59       234
17      0.80        0.65     0.71       224
18      0.39        0.40     0.39       197
19      0.27        0.33     0.30       132
------------------------------------------------
Accuracy: 0.51
Macro Avg: 0.51
Weighted Avg: 0.52


**SELF-IMPLEMENTATION**
Class   Precision   Recall   F1-Score   Support
------------------------------------------------
0       0.33        0.60     0.43       199
1       0.51        0.50     0.50       242
2       0.19        0.02     0.03       263
3       0.47        0.55     0.50       262
4       0.50        0.54     0.52       234
5       0.63        0.60     0.62       230
6       0.60        0.62     0.61       257
7       0.56        0.56     0.56       265
8       0.51        0.65     0.57       251
9       0.35        0.66     0.46       226
10      0.45        0.22     0.29       262
11      0.61        0.59     0.60       257
12      0.44        0.49     0.46       229
13      0.71        0.56     0.63       249
14      0.72        0.47     0.57       256
15      0.62        0.65     0.63       243
16      0.57        0.62     0.59       234
17      0.80        0.65     0.71       224
18      0.39        0.40     0.39       197
19      0.27        0.33     0.30       132
------------------------------------------------
Accuracy: 0.51
Macro Avg: 0.51
Weighted Avg: 0.52


## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details. 

## Acknowledgments
- The 20 Newsgroups dataset was collected by Ken Lang and is commonly used for experiments in text applications of machine learning techniques.
- The sklearn library provides easy-to-use machine learning tools for Python. 
- The nltk library is a leading platform for building Python programs to work with human language data. 

I hope this helps! If you have any questions, feel free to ask.
