## **Fake News Detection with Machine Learning**
This project uses Natural Language Processing (NLP) and various classification algorithms to distinguish between "Real" and "Fake" news articles. The primary goal is to build a model that learns the stylistic patterns and linguistic cues that differentiate genuine news reports from fabricated ones.

### **Project Overview**
The core of this project is a supervised learning task. We use a labeled dataset containing thousands of news articles and train several models to classify unseen articles. The process involves:

Data Loading & Preparation: Combining two datasets (True.csv and Fake.csv).

Text Preprocessing: Cleaning and normalizing the article text to prepare it for feature extraction.

Feature Engineering: Converting text into numerical vectors using the TF-IDF (Term Frequency-Inverse Document Frequency) technique.

Model Training: Building and training multiple classification models on the vectorized data.

Evaluation: Assessing model performance using accuracy scores and classification reports.

Manual Testing: Creating a function to classify new, user-provided articles.

### **Dataset**
The dataset consists of over 44,000 articles collected from various sources around 2017.

Genuine News: Sourced from Reuters.com, characterized by a formal, fact-based reporting style.

Fake News: Sourced from various outlets, often characterized by sensational, opinionated, or conspiratorial language.

### **Methodology**
Libraries: Pandas for data manipulation, Scikit-learn for machine learning, and re for regular expressions.

Preprocessing: A custom function was created to:

Convert text to lowercase.

Remove URLs, HTML tags, punctuation, and digits.

Vectorization: TfidfVectorizer was used to convert the cleaned text into a matrix of TF-IDF features, capturing the importance of each word in the corpus.

Models Trained:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Gradient Boosting Classifier

### **Results & Insights**
All trained models achieved a high accuracy of over 99% on the test set, demonstrating their ability to learn the distinct patterns of the two classes. However, manual testing revealed a crucial insight: the models are primarily stylistic pattern matchers, not fact-checkers. They heavily rely on cues like writing style (e.g., formal Reuters format) and the presence of sensational keywords, rather than the factual content of the news. This highlights the importance of understanding the limitations and biases of a model based on its training data.
