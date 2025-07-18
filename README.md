# Twitter Sentiment Analysis using Machine Learning

## 🔍 Problem Statement

Analyze and classify the sentiment of tweets into **positive** or **negative** categories using traditional NLP techniques and machine learning models.

---

## 📦 Dataset Used

* **Source:** Kaggle ([Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140))
* **Description:** Contains 1.6 million tweets with sentiment labels:

  * `0` = Negative
  * `4` = Positive
* Each tweet includes the text, tweet ID, date, flag, username, and label.

---

## ⚙️ Workflow Overview

### 1. Data Download & Setup

* Used Kaggle API to fetch the dataset.
* Extracted the `sentiment140.zip` and loaded the CSV file into a DataFrame.

### 2. Data Preprocessing

* Removed Twitter handles, URLs, special characters.
* Converted all text to lowercase.
* Tokenized tweets.
* Removed stopwords using `nltk`.
* Applied stemming using **PorterStemmer**.

### 3. Feature Engineering

* Used **TF-IDF Vectorizer** to convert text into numerical features.
* Limited the feature size for optimal model performance.

### 4. Model Training

* Split data into **training** and **testing** sets (typically 80/20).
* Used **Logistic Regression** from `sklearn` for classification.
* Evaluated using **accuracy score** and **confusion matrix**.

### 5. Model Persistence

* Trained model saved using `pickle` for future use.

---

## 📊 Results

* The Logistic Regression model performed well on preprocessed data.
* Text preprocessing and vectorization played a crucial role in boosting accuracy.

---

## 🧠 Learnings

* Traditional ML pipelines can still perform strongly for text tasks.
* Preprocessing heavily influences performance in sentiment analysis.
* TF-IDF works well as a baseline method.

---

## 🚀 Future Enhancements

* Use deep learning models like **LSTM**, **BERT**, or **DistilBERT** for better accuracy.
* Expand to **multi-class classification** (positive, neutral, negative, sarcastic).
* Analyze **emojis** and **hashtags** for improved sentiment cues.

---

## 📁 Folder Structure (Suggested)

```
TwitterSentiment/
├── NLP_twitter_tweets.ipynb
├── README.md
```

---

## 📈 Tools & Libraries

* `pandas`, `numpy`, `re`
* `nltk` (stopwords, stemming)
* `sklearn` (LogisticRegression, TfidfVectorizer, train\_test\_split, metrics)
* `pickle`

---

## 📅 Timeline Summary

* Dataset Download & Extraction ✅
* Preprocessing & Cleaning ✅
* Feature Engineering ✅
* Model Training ✅
* Model Evaluation ✅
* Model Saving ✅
