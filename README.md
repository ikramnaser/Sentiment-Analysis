# 📊 Sentiment Analysis with BERT

This project applies **state-of-the-art transformer models (BERT & DistilBERT)** to perform sentiment analysis on multilingual, timestamped social media data. It includes data preprocessing, visualization, and model preparation using the Hugging Face `transformers` library.

---

## 🧠 Objective

To classify social media posts into **Positive**, **Negative**, and **Neutral** sentiments using contextual language models (BERT and DistilBERT), and explore user behavior across countries, platforms, and time.

---

## 🗃️ Dataset Overview

The dataset consists of anonymized posts from multiple platforms (Twitter, Instagram, Facebook), with metadata such as:
- `Text`: The social media content
- `Sentiment`: Sentiment label (Positive/Negative/Neutral)
- `Timestamp`, `User`, `Platform`, `Country`, `Hashtags`, `Retweets`, `Likes`

📅 Temporal info was extracted from timestamps: Year, Month, Day, and Hour.

---

## ⚙️ Data Cleaning & Preprocessing

- Removed redundant columns 
- Stripped whitespace from all text columns
- Converted `Timestamp` to datetime and extracted `Year`, `Month`, `Day`
- Renamed columns for clarity

---

## 📊 Data Visualization

Exploratory Data Analysis (EDA) was performed using `Seaborn` and `Matplotlib`:

- **Sentiment distribution** across the dataset
- **Top countries** by volume of posts
- **Platform usage** distribution (Pie chart)
- **WordCloud** for most frequent words in posts

<div align="center">
  <img src="images/sentiment_distribution.png" alt="Sentiment Distribution" width="400"/>
  <img src="images/platform_pie.png" alt="Platform Usage" width="400"/>
</div>

---

## 🔍 NLP Modeling: BERT Tokenization

### Tokenization using `bert-base-cased`:
- Tokenized sentences into WordPieces
- Generated attention masks and input IDs
- Examined token length distribution (important for model padding/truncation)

### Tokenization using `distilbert-base-uncased`:
- Explored alternative model for lighter inference
- Compared tokenization outputs

> ⚠️ Migrated from deprecated `pad_to_max_length` to `padding='max_length'`

---

## 📦 Technologies Used

| Tool / Library    | Purpose                                |
|-------------------|----------------------------------------|
| `Pandas`          | Data cleaning and manipulation         |
| `Seaborn`, `Matplotlib` | Visualizations & plots          |
| `WordCloud`       | Text visualization                     |
| `transformers` by Hugging Face | Tokenization & model loading |
| `BERT`, `DistilBERT` | Transformer-based NLP models        |

---

## 🧩 Next Steps

- Fine-tune BERT on this dataset using a classification head
- Train/test split and model evaluation (Accuracy, F1-score)
- Hyperparameter tuning and experimentation with lightweight alternatives

---

## 🤝 Contributions

This project was developed as part of a portfolio for showcasing NLP and deep learning capabilities for sentiment analysis. It reflects practical skills in:
- End-to-end data preprocessing
- Applied NLP using transformers
- Visualization for insights extraction

---


