# AI-Driven-Sentiment-Analysis-for-BTC-Trends-Predictive-Approach-to-Crypto-Volatility-25307
## 📌 Project Overview

In the fast-paced and volatile world of cryptocurrency, investor sentiment can significantly influence market trends. This project leverages Natural Language Processing (NLP) and Machine Learning (ML) to analyze Twitter sentiments around Bitcoin and predict trends that could influence market volatility. 

We collected over 100,000 tweets containing keywords related to Bitcoin, performed sentiment classification (positive, neutral, negative), and evaluated multiple machine learning models to understand the sentiment landscape and its potential impact on crypto price movements.

---

## 📂 Dataset Description

The dataset contains the following fields:

| Column Name | Description |
|-------------|-------------|
| `id`        | Tweet ID |
| `user`      | Username of the author |
| `fullname`  | Full name of the author |
| `url`       | Tweet URL |
| `timestamp` | Time the tweet was posted |
| `replies`   | Number of replies |
| `likes`     | Number of likes |
| `retweets`  | Number of retweets |
| `text`      | Tweet content |

---

## ⚙️ Pipeline Summary

### 🔍 Preprocessing
- Removed links, hashtags, mentions, emojis, and special characters
- Applied tokenization, lemmatization, and stopword removal
- Created a new `clean_text` column for model input

### 📈 Feature Engineering
- Calculated `engagement = replies + likes + retweets`
- Extracted time features like hour and weekday

### 🧪 Sentiment Classification
- Sentiment labels were generated using `TextBlob`
- Three classes: **Positive (1)**, **Neutral (0)**, and **Negative (-1)**

### 📊 Visualizations
- Sentiment distribution pie chart
- Hourly tweet activity by sentiment
- Engagement heatmap (Day vs Hour)
- Top 20 users by average engagement
- Tweet length vs engagement scatterplot

---

## 🤖 Models Used & Comparison

We trained and evaluated three ML classifiers on the cleaned tweet data. Here’s a summary of their performance:

### ✅ Logistic Regression

| Metric        | Negative (-1) | Neutral (0) | Positive (1) |
|---------------|---------------|-------------|--------------|
| Precision     | 0.86          | 0.92        | 0.92         |
| Recall        | 0.64          | 0.98        | 0.91         |
| F1-score      | 0.73          | 0.95        | 0.92         |

- **Accuracy:** 91.7%
- **Macro Avg F1:** 87%
- **Weighted Avg F1:** 91%

---

### 🌲 Random Forest

| Metric        | Negative (-1) | Neutral (0) | Positive (1) |
|---------------|---------------|-------------|--------------|
| Precision     | 0.92          | 0.92        | 0.87         |
| Recall        | 0.52          | 0.97        | 0.93         |
| F1-score      | 0.67          | 0.95        | 0.90         |

- **Accuracy:** 90.4%
- **Macro Avg F1:** 84%
- **Weighted Avg F1:** 90%

---

### ⚙️ Support Vector Machine (LinearSVC)

| Metric        | Negative (-1) | Neutral (0) | Positive (1) |
|---------------|---------------|-------------|--------------|
| Precision     | 0.86          | 0.94        | 0.94         |
| Recall        | 0.71          | 0.98        | 0.93         |
| F1-score      | 0.78          | 0.96        | 0.93         |

- **Accuracy:** **93.17%**
- **Macro Avg F1:** 89%
- **Weighted Avg F1:** 93%

---

### 📊 Accuracy Comparison

| Model                  | Accuracy  |
|------------------------|-----------|
| Logistic Regression    | 91.70%    |
| Random Forest          | 90.40%    |
| Support Vector Machine | **93.17%** ✅ |

---

## 💼 Business Impact

### 📉 Predicting Market Sentiment
By monitoring Twitter sentiment, this model can serve as an early warning system for potential market volatility. Traders and investors can be alerted when public opinion shifts significantly positive or negative.

### 📊 Informed Decision-Making
- **Crypto Investors** can use sentiment trends to validate or reassess investment strategies.
- **Analysts & Exchanges** can monitor engagement peaks and user sentiment to explain sudden price fluctuations.

### 🧮 Quantifiable Insights
- Real-time sentiment scoring based on volume and type of tweets
- Integration with other market indicators for enhanced prediction


