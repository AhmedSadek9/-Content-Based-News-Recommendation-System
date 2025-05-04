# 📰 Content-Based News Recommendation System

This project implements a Content-Based Filtering Recommender System that suggests personalized news articles to users by analyzing article content and aligning it with user interests. Leveraging the MIND (Microsoft News Dataset), this system demonstrates core Natural Language Processing (NLP) and Information Retrieval techniques.

## 📌 Project Overview

The system recommends news articles based on content similarity between user preferences (e.g., keywords, categories) and article features such as titles and abstracts. It utilizes TF-IDF for feature extraction and cosine similarity for computing relevance.

### ✨ Key Features

- Preprocesses and extracts features from large-scale news data.
- Builds a user profile from selected interests or preferred articles.
- Computes content similarity to recommend relevant news items.
- Modular implementation using Jupyter notebooks.

## 🗂 Dataset

We use the [Microsoft News Dataset (MIND)](https://www.kaggle.com/datasets/arashnic/mind-news-dataset/data), which contains:
- `news.csv`: Contains metadata such as titles, abstracts, categories, and subcategories.

## 🛠️ Requirements

### Functional Requirements

- Load and preprocess MIND dataset.
- Extract TF-IDF features from article content.
- Construct a user profile vector based on preferences.
- Compute cosine similarity between user profile and articles.
- Recommend the top-N most relevant articles.

### Technical Requirements

**Programming Language:**  
- Python 3.x

**Python Libraries:**  
- `pandas`, `numpy`  
- `scikit-learn`  
- `NLTK` or `spaCy` (optional for preprocessing)  
- `matplotlib`, `seaborn` (optional for visualizations)

Install all dependencies using:

```bash
pip install -r requirements.txt
```

## 🧠 Project Structure

```plaintext
content_based_news_recommendation/
├── data/
│   └── news.csv                          # MIND dataset (article metadata)
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb       # Load and clean dataset; extract text features
│   ├── 02_user_profile_construction.ipynb# Build user profile vector
│   ├── 03_content_similarity.ipynb       # TF-IDF + cosine similarity
│   └── 04_ranking_and_recommendation.ipynb# Generate top-N recommendations
│
├── results/
│   ├── sample_recommendations.csv        # Sample output
│   └── user_feedback_notes.txt           # Optional notes/feedback
│
├── requirements.txt                      # Project dependencies
└── README.md                             # Project documentation
```

## 🚀 Getting Started

1. **Clone the repository**

```bash
git clone <your-repo-url>
cd content_based_news_recommendation
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Download the dataset**

Download from Kaggle: [MIND Dataset](https://www.kaggle.com/datasets/arashnic/mind-news-dataset/data)  
Place the `news.csv` file into the `data/` directory.

4. **Run notebooks**

Follow the notebooks in sequence inside the `notebooks/` folder.

## 📊 Sample Output

- Top recommended articles for user preferences (see `sample_recommendations.csv`)
- Visualizations and similarity heatmaps (optional)

## 📌 Future Improvements

- Incorporate implicit feedback (click history)
- Expand to hybrid recommender by combining collaborative filtering
- Integrate keyword extraction from user activity (e.g., browsing or search logs)
