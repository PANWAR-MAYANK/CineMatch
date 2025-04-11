# 🎬 CineMatch: The Ultimate Movie Recommendation Engine

Welcome to **CineMatch**, a powerful and intuitive content-based movie recommender system built using data science techniques and deployed via Streamlit. This project leverages the TMDB 5000 Movies Dataset to help users discover movies similar to their favorites, complete with stunning posters, metadata, and deep content analysis.

> ⚡ Live Demo: [Click to Explore CineMatch](https://cinematch-movies.streamlit.app/)

---

## 📌 Problem Statement

Finding a movie to watch can be overwhelming with the abundance of content available online. Traditional recommendations often fall short, failing to capture the nuanced preferences of users. **CineMatch** addresses this by offering intelligent, content-based movie recommendations using machine learning and natural language processing.

---

## 🚀 Features

✅ **Content-Based Filtering** using:
- Tags
- Keywords
- Cast
- Genre
- Production Companies

✅ **Top 25 Similar Movies** suggested based on cosine similarity  
✅ **Poster Retrieval** via TMDB API  
✅ **Detailed Metadata** like:
- Budget
- Runtime
- Release Date
- Languages
- Vote Ratings
- Cast and Director Information

✅ **Interactive Streamlit Interface**  
✅ **Caching and Pickling** for blazing-fast performance  

---

## 🧠 Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** | Core logic and scripting |
| **Pandas** | Data manipulation |
| **Scikit-learn** | Vectorization and similarity computations |
| **NLTK** | Stopword removal and stemming |
| **Streamlit** | UI & deployment |
| **Pickle** | Model and data serialization |
| **TMDB API** | Poster & person data |


---

## 🏗️ How It Works

1. **Data Preprocessing** (`preprocess.py`)
   - Extracts useful fields from raw TMDB data
   - Cleans and stems the data
   - Merges relevant metadata into a unified `tags` column

2. **Vectorization & Similarity Computation** (`display.py`)
   - Converts tags into vectors using `CountVectorizer`
   - Computes cosine similarity matrices for multiple features
   - Saves them using `pickle` for quick loading

3. **Recommendation Engine** (`preprocess.py`)
   - Retrieves similar movies by matching vectors
   - Fetches posters and metadata using the TMDB API

4. **Frontend App** (`main.py`)
   - Streamlit interface with dropdown selection
   - Displays recommendations with posters and details

---

## 🌐 TMDB API Configuration

This app uses the **TMDB API** to fetch movie posters and person details (cast, directors, etc.).

To avoid hitting rate limits or encountering API errors:

- 🔑 Use a **valid TMDB API key** in the `fetch_posters()` and `fetch_person_details()` functions inside `preprocess.py`.
- 🔁 Replace the placeholder or sample key.
- 🧠 Make sure to keep your API key private and avoid sharing it in public repositories.

---

## 🧪 Possible Improvements

- Add collaborative filtering using user ratings (Matrix Factorization or Surprise library)
- Enable filtering by language, decade, or streaming platforms
- Add genre-specific recommenders (e.g., Horror-only)
- Implement search and autocomplete for movie names
- Enable trailer view using Youtube API.

---

## 📈 Skills Demonstrated

- Machine Learning (Content-Based Filtering)
- NLP (Stemming, Stopword Removal, Vectorization)
- Web App Development (Streamlit)
- API Integration (TMDB)
- Data Serialization (Pickle)
- Modular and Scalable Code Design

---

## 🛠️ Installation & Setup Guide

To run **CineMatch** locally on your system, follow these simple steps:

---

### 🔁 1. Clone the Repository

```bash
git clone https://github.com/PANWAR-MAYANK/CineMatch.git
cd CineMatch
```


### 🐍 2. Create & Activate a Virtual Environment (Recommended)

For Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

For macOS/Linux:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 📦 3. Install the Required Dependencies

```bash
pip install -r requirements.txt
```

✅ Make sure you are connected to the internet during installation.


### 🔑 4. Add Your TMDB API Key

Open preprocess.py and replace with your personal TMDB API key from
https://www.themoviedb.org/settings/api.


### 🚀 5. Run the Streamlit App

```bash
streamlit run app.py
```



