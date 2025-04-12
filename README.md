# 🧠 Reddit Data Analysis

This project investigates Reddit discussions surrounding the **Israel-Hamas conflict** through topic modeling, named entity recognition (NER), sentiment analysis, and predictive modeling. It uses **natural language processing (NLP)** techniques to extract themes, analyze sentiment around key entities, and predict post popularity based on content.

---

---

## 📘 Project Tasks

### 🔹 Task 1: Topic Modeling

**Goal:** Discover underlying themes in Reddit posts using **Latent Dirichlet Allocation (LDA)**

**Steps:**
- Preprocessing: Lowercasing, removing mentions/URLs/special chars, lemmatization, and stopword removal.
- Vectorization: Using `CountVectorizer`.
- Topic Modeling: LDA with topics ranging from 1–10.
- Model Selection: Based on **Coherence Scores**.
- Visualization: Word clouds for each topic.

**Results:**
- **Topic 1**: Personal Experiences & Feelings — e.g., *feel, time, allah*
- **Topic 2**: Conflict & Politics — e.g., *israel, hamas, gaza, war*

---

### 🔹 Task 2: Named Entity Recognition (NER)

**Goal:** Analyze sentiment and context around key entities using **spaCy + VADER + NLTK**

**Entities Analyzed:**
- Israel  
- Hamas  
- Antony Blinken  
- Benjamin Netanyahu  
- IDF (Israeli Defense Forces)

**Steps:**
- NER: Entity extraction using spaCy.
- Sentiment Analysis: Compound VADER score for each sentence.
- POS Tagging: Extracting nouns, verbs, adjectives with NLTK.
- Visualization: Word clouds per entity and sentiment **boxplots**.

**Key Findings:**
- All entities had **predominantly negative sentiment**, with varying intensity.
- Word clouds revealed frequent context verbs (e.g., *attack*, *support*, *claim*) and nouns (e.g., *conflict*, *people*).

---

### 🔹 Task 3: Predicting Reddit Post Scores

**Goal:** Predict a Reddit post’s **score** (net upvotes) using ML models and text features.

**Feature Engineering:**
- Combined title and body of post.
- Cleaned and tokenized text.
- Topic distribution from LDA (3 features).
- Word2Vec embeddings (100-dimensions).

**Models Used:**
- **SVM (SVR)** with RBF kernel
- **XGBoost Regressor**

**Performance:**
| Model     | MSE        | R² Score |
|-----------|------------|----------|
| SVM       | 7900.22    | -0.0220  |
| XGBoost   | 7978.94    | -0.0322  |

**Conclusion:** Both models struggled to accurately predict post scores, likely due to the **unpredictability of virality** and missing non-textual features.

---

## 📊 Technologies Used

- Python (NLTK, spaCy, Gensim, Scikit-learn, XGBoost)
- LDA (Gensim)
- Word Embeddings: Word2Vec
- VADER Sentiment (NLTK)
- POS Tagging & NER (spaCy + NLTK)
- Data Visualization: Matplotlib, WordCloud

---

## 🔍 Key Learnings

- **LDA** effectively revealed latent topics within polarized discussions.
- NER combined with sentiment & POS tagging provided deep insights into **how entities are discussed**.
- Predicting Reddit **post score** purely from text remains challenging — future work could include temporal or user-based features.

---

## 📜 License

This project is intended for educational and academic use only.

---

## 🙌 Acknowledgments

- Reddit for open data  
- Virginia Tech CS Course  
- Libraries: spaCy, NLTK, VADER, Gensim, Scikit-learn, XGBoost



