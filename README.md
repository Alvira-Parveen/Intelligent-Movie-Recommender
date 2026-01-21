## 🎬 Intelligent Movie Recommendation System

An end-to-end **Movie Recommendation System** built from scratch, evolving from
simple baseline models to **industry-grade hybrid recommender systems**.

This project demonstrates not only *how recommendations are generated*, but also
*why certain models perform better*, including **error analysis**, **cold-start handling**,
and **real working recommendation examples**.

---

## 📌 Project Overview

This project implements a complete recommender system pipeline inspired by
real-world platforms such as **Netflix, Amazon, and Spotify**.

The system:
- Starts with simple baseline approaches
- Progresses through collaborative filtering
- Uses matrix factorization (SVD)
- Implements an industry-standard Surprise SVD model
- Solves the cold-start problem using a hybrid strategy
- Demonstrates actual movie recommendations for users

---

## 🎯 Objectives

- Build multiple recommendation models
- Compare models using RMSE
- Analyze model errors and limitations
- Study the cold-start problem
- Design a hybrid recommender system
- Provide a real, user-facing recommendation demo

---

## 🧠 Recommendation Techniques Implemented

### 1️⃣ Baseline Models
- Global Average Rating
- Movie Average Rating

### 2️⃣ Collaborative Filtering
- User-Based Collaborative Filtering
- Item-Based Collaborative Filtering

### 3️⃣ Matrix Factorization
- Singular Value Decomposition (SVD)

### 4️⃣ Surprise SVD (Industry Standard)
- Bias terms (user & item bias)
- Regularization
- Stochastic Gradient Descent optimization

### 5️⃣ Hybrid Recommendation System
- Combines:
  - Collaborative Filtering (SVD)
  - Content-Based Filtering (Movie Genres)
- Designed to handle **cold-start users**

---

## 📊 Dataset

- **MovieLens Dataset**
- Files used:
  - `ratings.csv`
  - `movies.csv`
- Explicit ratings on a 0.5–5.0 scale

---

## 🗂️ Project Structure

recommender-research/
│
├── data/
│   ├── ratings.csv
│   └── movies.csv
│
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   ├── 02_baseline_models.ipynb
│   ├── 03_user_item_cf.ipynb
│   ├── 04_matrix_factorization.ipynb
│   ├── 05_surprise_svd.ipynb
│   ├── 06_error_analysis.ipynb
│   ├── 07_cold_start_analysis.ipynb
│   ├── 08_hybrid_recommender.ipynb
│   ├── 09_final_comparison.ipynb
│   └── 10_conclusion.ipynb
│
├── venv/
├── README.md
└── requirements.txt


---

## ⚙️ Technologies Used

- Python 3
- Pandas
- NumPy
- Scikit-learn
- Scikit-Surprise
- Matplotlib
- Jupyter Notebook

---

## 📈 Model Performance (RMSE)

| Model | RMSE |
|-----|-----|
| Global Average | ~1.05 |
| Movie Average | ~0.98 |
| User-Based CF | ~0.92 |
| Item-Based CF | ~0.90 |
| Surprise SVD | **~0.88 (Best)** |
| Hybrid (SVD + Content) | ~0.88 |

✔ Surprise SVD achieved the best overall accuracy  
✔ Hybrid model improves robustness in cold-start scenarios

---

## ❄️ Cold-Start Analysis

### Problem
Collaborative filtering relies on historical interactions, which causes poor
performance for:
- New users
- Infrequent users
- New items

### Findings
- Cold users exhibit significantly higher prediction error
- Popular items are easier to predict
- Sparse interaction history degrades performance

### Solution
A **Hybrid Recommendation System** was implemented that falls back to
content-based filtering when collaborative filtering fails.

---

## 🎥 Real Working Recommendation Examples

### 🎯 Recommendation for an Existing User

```python
recommend_movies(user_id=1, n=10)

## Example Output
- The Shawshank Redemption (1994)
- The Godfather (1972)
- Casablanca (1942)
- Rear Window (1954)
- Lawrence of Arabia (1962)

## 🆕 Cold-Start Recommendation (New User)

cold_start_recommend(n=10)  # Returns the most popular and highly rated movies.

## 🎭 Genre + Liked Movie Based Recommendation

recommend_movies_genre_and_liked(
    liked_titles=["Inception (2010)", "The Dark Knight (2008)"],
    preferred_genres=["Sci-Fi", "Thriller"],
    n=10
)                    # This mimics real-world user preference based recommendation.

## 🧩 Hybrid Recommendation Logic

- If user history exists → Use Surprise SVD
- If SVD prediction unavailable → Use Genre-Based Content Filtering
- If user is completely new → Use Popularity-Based Recommendation

---

## 🔍 Key Insights

- Matrix factorization outperforms neighborhood-based methods
- Cold-start remains a fundamental recommender challenge
- Hybrid systems improve robustness
- Evaluation and error analysis are critical for real systems

---

## 🏁 Conclusion

This project demonstrates the complete lifecycle of a recommender system:
from theory and modeling to evaluation, analysis, and real recommendation output.

The final system is: Research-oriented
                     Production-inspired
                     Robust to cold-start
                     Capable of generating real movie recommendations

---

## 🚀 Future Improvements

- Streamlit / Web-based UI
- Deep learning based recommenders
- User feedback loop
- API deployment (FastAPI / Flask)

---

## 👩‍💻 Author

**Name**: ALVIRA PARVEEN  
🔗 [LinkedIn](https://www.linkedin.com/in/alvira-parveen-78022536b)  
🌐 [GitHub](https://github.com/Alvira-Parveen)
