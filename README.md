# Text Classification Project

This project is a text classification task using the 20 Newsgroups dataset. The goal is to classify a given text into one of 20 categories.

## Table of Contents
1. [Dependencies](#dependencies)
2. [Dataset Description](#dataset-description)
3. [Data Preprocessing](#data-preprocessing)
4. [Model Training and Evaluation](#model-training-and-evaluation)
5. [Custom Implementation of Naive Bayes](#custom-implementation-of-naive-bayes)
6. [Comparison of SKlearn vs Own Implementation](#comparison-of-sklearn-vs-own-implementation)
7. [License](#license)
8. [Acknowledgments](#acknowledgments)

## Dependencies
The project requires the following Python libraries:
- numpy
- pandas
- sklearn
- nltk

## Dataset Description
The 20 Newsgroups dataset is a collection of approximately 20,000 newsgroup documents, partitioned (nearly) evenly across 20 different newsgroups. The data is organized into 20 different newsgroups, each corresponding to a different topic. Some of the newsgroups are very closely related to each other (e.g. comp.sys.ibm.pc.hardware, comp.sys.mac.hardware), while others are highly unrelated (e.g misc.forsale, soc.religion.christian).

## Data Preprocessing
The data preprocessing involves several steps:

1. **Tokenization**: The text is split into individual words using the `tokenize` function.

2. **Stopword Removal**: Common words that do not contain important meaning are removed using the nltk library's list of English stop words.

3. **Word Lemmatization**: Lemmatization reduces words to their base or root form, which helps in reducing the feature space and capturing the essence of words. In this project, the WordNet lemmatizer from the nltk library is used for this step.
4. Lemmatization is a linguistic process that reduces words to their base or root form, known as the lemma. It aims to transform different inflected forms of a word into a single, canonical form. For example, the lemma of "running" is "run", the lemma of "mice" is "mouse", and so on.

Here's why lemmatization is important in natural language processing tasks:

1. **Normalization**: Lemmatization helps in normalizing words by reducing them to their base form. This is essential for ensuring consistency in text data, as different inflected forms of words may occur in different contexts.

2. **Reduced Feature Space**: By reducing words to their base form, lemmatization helps in reducing the feature space in text data. This is particularly important for tasks such as text classification or clustering, where the number of features (words) can be very large. By lemmatizing words, we can represent variations of the same word with a single feature, leading to more efficient and effective models.

3. **Improved Accuracy**: Lemmatization can lead to improved accuracy in natural language processing tasks. By mapping different inflected forms of a word to the same lemma, lemmatization helps in capturing the underlying meaning or semantics of the text more accurately. This is especially beneficial for tasks such as sentiment analysis, where understanding the meaning of words is crucial for determining sentiment.

4. **Better Interpretability**: Lemmatization can also improve the interpretability of text data. By reducing words to their base form, the resulting text representations are often more intuitive and easier to interpret. This can be useful for tasks such as topic modeling or text summarization, where understanding the underlying content of the text is important.

Overall, lemmatization plays a crucial role in natural language processing tasks by normalizing text data, reducing the feature space, improving accuracy, and enhancing interpretability. It is an essential preprocessing step in many NLP pipelines and helps in extracting meaningful insights from text data.

5. **Term Frequency-Inverse Document Frequency (TF-IDF)**:

### Term Frequency (TF):
Term Frequency measures how often a term occurs in a document. It is calculated by dividing the number of occurrences of a term in a document by the total number of terms in the document.

Mathematically, TF is calculated as follows for a term \( t \) in a document \( d \):

\[
TF(t, d) = \frac{\text{Number of occurrences of term } t \text{ in document } d}{\text{Total number of terms in document } d}
\]

### Inverse Document Frequency (IDF):
Inverse Document Frequency measures how important a term is across multiple documents in a corpus. It is calculated by taking the logarithm of the ratio of the total number of documents in the corpus to the number of documents containing the term, and then adding 1 to avoid division by zero for terms that appear in all documents.

Mathematically, IDF is calculated as follows for a term \( t \) in a corpus:

\[
IDF(t) = \log{\left(\frac{\text{Total number of documents in the corpus}}{\text{Number of documents containing term } t} + 1\right)}
\]

### TF-IDF:
TF-IDF is the product of Term Frequency and Inverse Document Frequency. It gives a higher weight to terms that are frequent in a document but rare across the corpus. This helps in identifying important terms in a document.

Mathematically, TF-IDF is calculated as follows for a term \( t \) in a document \( d \):

\[
TF-IDF(t, d) = TF(t, d) \times IDF(t)
\]

## Model Training and Evaluation
The Multinomial Naive Bayes model from sklearn is used for training. The model is trained on the TF-IDF transformed training data and then used to predict the categories of the TF-IDF transformed test data. The performance of the model is evaluated using a confusion matrix.
![image](https://github.com/javarath/TEXT-CLASSIFICATION-OWN-IMPLEMENTATION-VS-SKLEARN-IMPLEMENTATION-/assets/102171533/11cd9411-8f18-4eb2-92c4-5c4502166470)
![image](https://github.com/javarath/TEXT-CLASSIFICATION-OWN-IMPLEMENTATION-VS-SKLEARN-IMPLEMENTATION-/assets/102171533/4888a94a-5448-40a3-8b81-af6e1a3f8f28)


## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details. 

## Acknowledgments
- The 20 Newsgroups dataset was collected by Ken Lang and is commonly used for experiments in text applications of machine learning techniques.
- The sklearn library provides easy-to-use machine learning tools for Python. 
- The nltk library is a leading platform for building Python programs to work with human language data. 

This detailed readme provides insights into the text classification project and its components. If you have any questions, feel free to ask.
