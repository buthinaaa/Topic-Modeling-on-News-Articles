# Topic-Modeling-on-News-Articles

A comparative analysis of **Latent Dirichlet Allocation (LDA)** and **Non-Negative Matrix Factorization (NMF)** for unsupervised topic modeling on the BBC News dataset — completed as part of the **Elevo Pathway Internship**.

## 🎯 Objective
Discover hidden thematic structures in 2,225 unlabeled BBC news articles across 5 categories:
- Business  
- Entertainment  
- Politics  
- Sport  
- Tech  

Using **only the text**, we extract and compare interpretable topics **without using labels during training**.

## 🔍 Key Findings

✅ **NMF outperforms LDA** on this dataset:
- **Sport**: 501/503 articles mapped to a single NMF topic  
- **Politics**: 381/403 articles concentrated in one topic  
- **Tech & Entertainment**: Strong topic purity  

⚠️ **LDA shows topic mixing**: Business, politics, and tech articles are split across multiple topics, reducing interpretability.

💡 **Why?**  
News articles are short and keyword-driven — ideal for **NMF + TF-IDF**, which emphasizes discriminative terms. LDA’s probabilistic word mixtures are less effective here.

> **Conclusion**: For short, category-driven texts like news headlines, **NMF is the superior choice**.

## 🛠️ Tools & Libraries
- **Python**  
- **Gensim** (LDA)  
- **scikit-learn** (NMF, TF-IDF)  
- **spaCy** (lemmatization)  
- **pyLDAvis** (interactive LDA visualization)  
- **WordCloud** (topic visualization)  
- **Pandas, NumPy, Matplotlib**

## 📁 Project Structure
```
.
├── bbc_news_topic_modeling.ipynb   # Main notebook
├── README.md
└── requirements.txt                # Dependencies
```

## ▶️ How to Run

1. **Clone the repo**
   ```bash
   git clone ttps://github.com/buthinaaa/Topic-Modeling-on-News-Articles.git
   cd Topic-Modeling-on-News-Articles
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download the dataset**  
   The notebook uses the [BBC Articles Dataset](https://www.kaggle.com/datasets/jacopoferretti/bbc-articles-dataset) from Kaggle.  

4. **Run the notebook**  
   Open `Topic-Modeling-on-BBC-News-Articles.ipynb` in Jupyter or Google Colab.

> 💡 **Note**: The notebook includes full preprocessing, modeling, visualization, and evaluation.

## 📊 Visualizations Included
- **Interactive LDA topics** via `pyLDAvis`  
- **Side-by-side word clouds** for LDA and NMF (2×3 grid)  
- **Label alignment tables** comparing model performance

## 🙌 Acknowledgements
- Dataset: [BBC Articles Dataset (Kaggle)](https://www.kaggle.com/datasets/jacopoferretti/bbc-articles-dataset)  
- Internship: [Elevo Pathway Program](https://elevo.ai/)  


---
