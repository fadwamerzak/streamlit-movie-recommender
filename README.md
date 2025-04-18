# 🎬 Movie Recommender System

A simple and intuitive **Movie Recommender System** built using **Python** and **Streamlit**, based on **content-based filtering** techniques. It recommends movies similar to the ones you like, based on metadata such as genres, keywords, cast, and more.

## 📌 Features

- ✅ Recommends movies based on textual similarity
- ✅ Uses **CountVectorizer** to create a bag-of-words model from movie metadata
- ✅ Content-based filtering (no need for user ratings)
- ✅ Streamlit-powered web interface for interactive exploration
- ✅ Lightweight and easy to run locally

---

## 🧠 How It Works

1. **Data Preprocessing**:
   - Combined relevant features (`overview`, `genres`, `keywords`, `cast`, `crew`) into a single `tags` column.
   - Removed stop words and applied basic NLP techniques.

2. **Vectorization**:
   - Used **`CountVectorizer`** from `sklearn` to convert the `tags` text into a numerical matrix (bag-of-words model).
   - Limited the vocabulary to the top 5000 frequent words for performance.

3. **Similarity Calculation**:
   - Computed **cosine similarity** between all movie vectors.
   - Stored the similarity matrix in a `.pkl` file for quick loading.

4. **Recommendation**:
   - When a user inputs a movie title, the app retrieves its vector and finds the most similar movies based on cosine distance.

---

## 📷 App Preview
<img width="731" alt="Screenshot 2025-04-18 093022" src="https://github.com/user-attachments/assets/b70c4fd4-f78e-4021-95d4-f7a745285961" />
<img width="651" alt="Screenshot 2025-04-18 093116" src="https://github.com/user-attachments/assets/158e02d6-5d62-4971-902f-64cf13723975" />


---

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3.x
- pip
- [Streamlit](https://streamlit.io/)
- Other dependencies: `pandas`, `numpy`, `scikit-learn`

### ⚙️ Installation

```bash
# Clone the repo
git clone https://github.com/fadwamerzak/streamlit-movie-recommender.git
cd streamlit-movie-recommender

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
