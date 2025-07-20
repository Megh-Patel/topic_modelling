# 🧠 Topic Modeling on BBC News Articles

This project applies unsupervised machine learning techniques to uncover hidden thematic structures in a corpus of ~1,500 BBC news articles. Using both **Latent Dirichlet Allocation (LDA)** and **Non-negative Matrix Factorization (NMF)**, the project aims to generate interpretable topics that align with real-world news categories.

---

## 📌 Project Objectives

- Automatically discover dominant topics within BBC news articles
- Compare LDA and NMF topic modeling techniques
- Evaluate topic quality using coherence scores, perplexity, and reconstruction error
- Visualize topic-word distributions and document clusters

---

## 🗃 Dataset

- **Source:** - BBC News Dataset
- **Size:** ~1,500 articles
- **Categories:** Sport, Business, Politics, Tech, Entertainment

---

## ⚙️ Workflow

### 1. Text Preprocessing
- Expanded contractions
- Lowercased text
- Removed punctuation, digits, and extra whitespace
- Removed stopwords (including custom additions)
- Lemmatized using WordNetLemmatizer

### 2. Vectorization
- `CountVectorizer` for LDA
- `TfidfVectorizer` for NMF
- Tuned `max_df` and `min_df` to filter noisy terms

### 3. Model Training & Evaluation
- Trained 6 LDA models (varying topics & learning_decay)
- Trained 6 NMF models (varying number of topics)
- Evaluated using:
  - **LDA:** Perplexity + Coherence Score
  - **NMF:** Reconstruction Error + Coherence Score
- Visualized with:
  - **t-SNE** for document-topic clustering
  - **pyLDAvis** for LDA topic-word relationships

---

## 🏆 Best Performing Model

- **Model Type:** NMF  
- **Number of Topics:** 5  
- **Coherence Score:** **0.76**  
- **Highlights:** Produced clear, non-overlapping topics closely aligned with actual BBC categories like business, politics, entertainment, tech, and sports.

---

## 📊 Visualizations

- Topic-wise top terms
- pyLDAvis interactive dashboard for LDA
- t-SNE plots of clustered documents



## 🛠 Tools & Libraries

- Python
- Pandas, NumPy
- Scikit-learn
- Gensim
- Matplotlib, Seaborn
- pyLDAvis
- NLTK

---

## 📁 Repository Structure

```bash
📦topic-modeling-bbc
 ┣ 📜bbc_news.csv
 ┣ 📜Topic_Modeling_BBC.ipynb
 ┣ 📜README.md
