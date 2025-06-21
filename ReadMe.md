# Movie Recommender CLI

A simple, interactive movie recommendation system using TF-IDF and collaborative filtering, built with Python and Jupyter Notebook. This project demonstrates how to use text-based search and user ratings to recommend movies from the [MovieLens 25M dataset](https://grouplens.org/datasets/movielens/25m/).

---

## Features

- **TF-IDF Search:**
  - Search for movies by title using TF-IDF vectorization and cosine similarity.
- **Collaborative Filtering:**
  - Recommend movies based on what similar users liked, using user ratings and popularity ratios.
- **Interactive UI:**
  - Simple text input and live recommendations using Jupyter widgets.

---

## How It Works

1. **TF-IDF Vectorization:**
   - Movie titles are cleaned and vectorized using `TfidfVectorizer` (with unigrams and bigrams).
   - Cosine similarity is used to find the closest matches to a user's search query.
2. **Collaborative Filtering:**
   - For a selected movie, the system finds users who rated it highly.
   - It then recommends other movies that these users also liked, prioritizing those that are more popular among similar users than the general population.
3. **Interactive Experience:**
   - Enter a movie title in the input box to see matching movies and recommendations update live.

---

## Setup & Requirements

- Python 3.7+
- Jupyter Notebook (or JupyterLab)
- Required packages:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `requests`
  - `ipywidgets`

Install dependencies (if not already installed):

```bash
pip install pandas numpy scikit-learn requests ipywidgets
```

---

## Usage

1. **Open the Notebook:**
   - Launch Jupyter Notebook and open `movie_recommendations.ipynb`.
2. **Run All Cells:**
   - The notebook will automatically download and extract the MovieLens 25M dataset if not present.
   - Wait for the data to download and extract (first run only).
3. **Search & Get Recommendations:**
   - Enter a movie title (e.g., `Toy Story`) in the input box.
   - The notebook will display matching movies and a list of recommended movies based on collaborative filtering.

---

## Project Structure

- `movie_recommendations.ipynb` — Main notebook with all code and UI.
- `ReadMe.md` — This file.

---

## Notes

- The dataset is large (~700MB zipped, ~4GB unzipped). Ensure you have enough disk space and a stable internet connection for the initial download.
- The UI is designed for Jupyter Notebook and uses `ipywidgets` for interactivity.
- Recommendations are based on ratings above a threshold (default: 4.0) and popularity among similar users.

---

## Acknowledgements

- [MovieLens 25M Dataset](https://grouplens.org/datasets/movielens/25m/) by GroupLens
- Built with [scikit-learn](https://scikit-learn.org/), [pandas](https://pandas.pydata.org/), and [ipywidgets](https://ipywidgets.readthedocs.io/) 