# AI-Systems-Development


### Name : Kusum Patel

### Branch : DSAI

### Roll No. : 221020436


# 🎬 Semantic Search on Movie Plots

This project implements a **semantic search engine** in Python to find movies based on plot similarity. It uses **Sentence Transformers** to generate embeddings for movie plots and **cosine similarity** to retrieve the most relevant results.

---

## ✅ Features

- Embedding generation using pre-trained transformer models from `sentence-transformers`.
- Cosine similarity for semantic search, ensuring context-based matching.
- Easily extendable to other datasets like books, articles, or product descriptions.

---

## ⚙️ Installation & Setup

Follow these steps to set up and run the project locally:

### 1. Clone the repository

```bash
git clone <https://github.com/kuzum09/Ai-System-Devlopment-Assignemnt-1/tree/main>
cd <project-directory>
```



### 2. Create and activate a virtual environment

**On macOS/Linux:**

```bash
python3 -m venv venv
source venv/bin/activate
```

**On Windows:**

```bash
python -m venv venv
.\venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the example script

```bash
python movie_search.py
```

---

## 🧪 Testing

To run unit tests and ensure everything works correctly:

```bash
python -m unittest discover -v
```

---

## 💻 Usage

You can integrate the `search_movies()` function into your own scripts:

```python
from movie_search import search_movies

query = 'a spy thriller in Paris'
results = search_movies(query=query, top_n=3)

print(f"Search results for: '{query}'")
for r in results:
    print(r)
```

---

## 📂 Project Structure

```
├── movie_search.py      # Core semantic search logic
├── movies.csv           # Dataset of movie plots
├── requirements.txt     # Project dependencies
├── tests/               # Unit tests
└── README.md            # Project documentation
```

---

## 🔍 How It Works

1. **Load Data:** Reads movie titles and plots from a CSV file.
2. **Generate Embeddings:** Uses a pre-trained transformer model (e.g., `all-MiniLM-L6-v2`) to convert plots into numerical vectors.
3. **Similarity Calculation:** Computes cosine similarity between the query and all movie embeddings.
4. **Return Results:** Sorts and returns the top N most relevant movies.

---

✅ **Tip:** You can replace `movies.csv` with your own dataset or change the embedding model in `movie_search.py` for better results.

---

### 🛠 Tech Stack

- **Python 3.8+**
- **Sentence Transformers**
- **scikit-learn** for cosine similarity
- **pandas & numpy** for data handling

```

