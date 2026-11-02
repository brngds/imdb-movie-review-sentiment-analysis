# 🎬 IMDb Movie Review Sentiment Analysis

### 🧠 Natural Language Processing | Machine Learning | Sentiment Classification

An end-to-end NLP project focused on automatically classifying IMDb movie reviews as **positive or negative**, using text preprocessing, TF-IDF, machine learning and BERT embeddings.

**🏆 Best F1 Score: 0.88 | 🎯 Target: ≥ 0.85**

---

## 📌 Project Overview

Film Junky Union is building an automated sentiment analysis system to identify negative movie reviews and improve content categorization.

This project explores different NLP techniques and machine learning algorithms to determine which approach provides the most reliable sentiment predictions.

### 🎯 Business Objectives

- Automatically classify positive and negative movie reviews.
- Identify negative feedback efficiently.
- Compare traditional NLP and transformer-based approaches.
- Achieve an **F1 score of at least 0.85**.

---

## 📊 Dataset

The dataset contains **47,331 IMDb movie reviews**, including sentiment labels and predefined training and testing partitions.

| Feature | Description |
|---|---|
| `review` | Movie review text |
| `pos` | Sentiment label: 0 = Negative, 1 = Positive |
| `ds_part` | Dataset partition: train or test |

**📂 Original dataset:** `imdb_reviews.tsv`

The dataset is split into smaller files for GitHub compatibility and reconstructed during notebook execution.

**Source:** Maas et al. (2011), *Learning Word Vectors for Sentiment Analysis*.

---

## 🔍 Exploratory Data Analysis

The exploratory analysis includes:

- Data quality and missing-value checks.
- Sentiment distribution and class balance.
- Review volume across training and test partitions.
- Review length and temporal patterns.

The analysis helps identify dataset characteristics that may influence classification performance.

---

## ⚙️ NLP Pipeline

The text processing workflow includes:

1. 🧹 **Text Cleaning:** Normalize text and remove unnecessary characters.
2. 🔤 **Tokenization:** Break reviews into meaningful text units.
3. 📚 **Lemmatization:** Normalize words using NLTK and spaCy approaches.
4. 📐 **TF-IDF Vectorization:** Transform text into numerical features.
5. 🤖 **Model Training:** Train and evaluate sentiment classifiers.
6. 📈 **Evaluation:** Compare F1, ROC-AUC and other classification metrics.

A separate experiment explores contextual embeddings generated using BERT.

---

## 🤖 Machine Learning Models

| Model | Test F1 | Test ROC-AUC |
|---|---:|---:|
| Constant Baseline | 0.00 | 0.50 |
| NLTK + TF-IDF + Logistic Regression | **0.88** | **0.95** |
| spaCy + TF-IDF + Logistic Regression | **0.88** | **0.95** |
| spaCy + TF-IDF + LightGBM | 0.84 | 0.92 |
| BERT Embeddings + Logistic Regression | 0.77 | 0.90 |

### 🏆 Best Performing Models

**Logistic Regression with TF-IDF** achieved the strongest test results, reaching an F1 score of approximately **0.88**.

Both the NLTK-based and spaCy-based approaches exceeded the required F1 threshold of 0.85.

**⚠️ BERT experiment:** The BERT model was evaluated on a limited sample of 200 training reviews and 200 test reviews due to computational constraints. Its performance is not directly comparable with full-dataset results.

---

## 🧪 Custom Review Predictions

Eight manually written movie reviews were used to evaluate how the models classify previously unseen examples.

This qualitative experiment helps explore model behavior beyond the numerical evaluation metrics.

---

## 💡 Key Findings

- ✅ The required F1 score of 0.85 was achieved.
- ✅ TF-IDF combined with Logistic Regression provided strong classification performance.
- 📚 spaCy lemmatization reduced vocabulary size while maintaining competitive results.
- 📉 LightGBM achieved a lower F1 score than the best Logistic Regression models.
- 🧠 The limited BERT experiment demonstrated the challenges of training with small samples.
- 🎯 Traditional NLP approaches proved effective for this binary sentiment classification task.

---

## 🚀 Business Impact

An automated sentiment classification system can help Film Junky Union:

- Identify negative reviews more efficiently.
- Automate large-scale review categorization.
- Monitor audience sentiment.
- Reduce manual moderation workload.
- Support data-driven content analysis.

---

## 🛠️ Technologies & Tools

**Programming & Data Analysis**

- 🐍 Python
- 🐼 Pandas
- 🔢 NumPy
- 📊 Matplotlib

**Natural Language Processing**

- NLTK
- spaCy
- TF-IDF
- Hugging Face Transformers

**Machine Learning**

- Scikit-learn
- Logistic Regression
- LightGBM
- BERT
- PyTorch

**Development Environment**

- Jupyter Notebook
- Git & GitHub

---

## 📁 Repository Structure

```text
imdb-movie-review-sentiment-analysis/
│
├── 📄 README.md
│
├── 📂 data/
│   ├── README.md
│   └── imdb_reviews_part_*.tsv
│
└── 📂 notebook/
    ├── README.md
    └── imdb_sentiment_analysis.ipynb
```

---

## ▶️ How to Run

1. Clone the repository.
2. Install the required Python dependencies.
3. Place all dataset parts inside the `data/` directory.
4. Open `notebook/imdb_sentiment_analysis.ipynb`.
5. Execute the notebook cells in sequence.

The prepared notebook reconstructs the original dataset from the uploaded parts.

**Note:** The BERT experiment may require additional computational resources.

---

## ⚠️ Limitations & Future Improvements

- Evaluate performance on movie reviews from other platforms.
- Explore advanced transformer-based architectures.
- Improve classification of sarcasm and ambiguous language.
- Test model performance on newer reviews.
- Evaluate model deployment through a prediction API.

---

## 📚 Dataset Reference

Maas, A. L., Daly, R. E., Pham, P. T., Huang, D., Ng, A. Y., & Potts, C. (2011).

*Learning Word Vectors for Sentiment Analysis.*

Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics (ACL 2011).

---

## 👨‍💻 Author

**Brunno Almeida**

Data Science | Data Analytics | Python | SQL | Machine Learning

*Building practical, data-driven solutions through analytics and machine learning.*
