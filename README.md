# sentimental-analysis
# 📊 Twitter Sentiment Analysis using LSTM (Sentiment140 Dataset)

This repository contains an end-to-end project for performing **Sentiment Analysis on Tweets** using the [Sentiment140 dataset](http://help.sentiment140.com/home). The pipeline uses **data preprocessing, tokenization, and a deep learning model (LSTM)** built with TensorFlow/Keras.

---

## 🗂️ Dataset

The Sentiment140 dataset consists of **1.6 million labeled tweets** extracted via the Twitter API. The tweets are labeled as:

- `0` → Negative sentiment  
- `2` → Neutral sentiment (not used in this project)  
- `4` → Positive sentiment

In this project, we map:  
- `4` ➝ `1` (Positive)  
- `0` ➝ `0` (Negative)  

Each record in the dataset contains:
1. `target` - Sentiment label (0 or 4)  
2. `ids` - Tweet ID  
3. `date` - Date of the tweet  
4. `flag` - Query (e.g., `NO_QUERY`)  
5. `user` - Username  
6. `text` - Tweet content  

**Citation**:  
> Go, A., Bhayani, R., & Huang, L. (2009). *Twitter Sentiment Classification using Distant Supervision*. CS224N Project Report, Stanford.

---

## 🚀 Features

- Cleaned text using:
  - Stopword removal
  - Punctuation removal
  - URL, email, and number removal
  - Tokenization
  - Lemmatization
- Built an LSTM model using TensorFlow and Keras
- Visualized model performance

---

## 🛠️ Technologies Used

- Python  
- Pandas, NumPy, Matplotlib, Seaborn  
- Scikit-learn  
- TensorFlow & Keras  
- NLTK (for NLP tasks)  
- MLXtend (for confusion matrix)  

---

## 🧪 Model Architecture

Input (500 padded tokens)
↓
Embedding Layer (2000 vocab, 50 dim)
↓
LSTM (64 units)
↓
Dense (256) + ReLU Activation
↓
Dropout (0.5)
↓
Dense (1) + Sigmoid Activation
↓
Binary Classification (Positive / Negative)

yaml
Copy code
