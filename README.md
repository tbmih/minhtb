# Machine-Learning-for-Phishing-URL-Detection
 - **Data Source**
   * Phishtank.org
   * Hackertarget.com
 - **Description**
   * This project aims to detect fraudulent URLs using Machine Learning models. To enhance the detection process, Natural Language Processing (NLP) techniques are applied. The combination of these methods improves the ability to identify potentially deceptive URLs in a sophisticated and user-friendly manner.
 - **Objective**:
Identify the algorithm and model that yield the best results based on 4 evaluation criteria:
   * Accuracy
   * Precision
   * Recall
   * F1 Score
 - **Data**
   * The data consists of 2 fields: URL and labels collected from two sources, Phishtank.org and Hackertarget.
   * Two natural language processing methods are used: TfidfVectorizer and Countvectorizer.
- **Technology Used:** Python
- **Results** : Best Model and Processing Method
  * MultinomialNB trained with the Countvectorizer dataset
    + Accuracy: 0.8578
    + Precision: 0.8941
    + Recall: 0.8248
    + F1 Score: 0.8581
  * MultinomialNB trained with the TfidfVectorizer dataset
    + Accuracy: 0.8633
    + Precision: 0.8983
    + Recall: 0.8318
    + F1 Score: 0.8638
  * LogisticRegression trained with the Countvectorizer dataset
    + Accuracy: 0.8487
    + Precision: 0.9600
    + Recall: 0.7406
    + F1 Score: 0.8362
  * LogisticRegression trained with the TfidfVectorizer dataset
    + Accuracy: 0.8487
    + Precision: 0.9188
    + Recall: 0.7396
    + F1 Score: 0.8412
 - **Conclusion** :
   + MultinomialNB (Multinomial Naive Bayes) assumes that the input features are extracted from a multinomial distribution. This is useful in tasks counting the occurrences of words in text
   +  LogisticRegression is based on the logistic distribution and assumes that the probability of a sample belonging to the positive class is described by the sigmoid function of the input features.
 - In this case, MultinomialNB is somewhat more suitable.
   +  CountVectorizer treats all words as important, regardless of whether they appear frequently or infrequently in the entire dataset.
   +  TfidfVectorizer gives higher IDF values to common words (appearing in many documents), reducing their importance in the representation vector. Rare words that appear in a few documents receive higher IDF values, improving text identification. In this case, CountVectorizer and TfidfVectorizer are evaluated equally.
