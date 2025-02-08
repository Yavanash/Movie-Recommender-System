# Movie Recommender System

A content-based movie recommendation system that suggests similar movies based on plot, genres, cast, crew, and keywords. The system uses natural language processing and machine learning techniques to analyze movie features and find similarities.

## Features

- Content-based movie recommendation using multiple movie attributes
- Processes movie data from TMDB dataset
- Uses cosine similarity to find movie relationships
- Handles text processing with stemming and vectorization
- Returns top 5 similar movie recommendations

## Technologies Used

- Python 3.x
- Pandas: Data manipulation and analysis
- NumPy: Numerical computing
- Scikit-learn: Machine learning tools
- NLTK: Natural Language Processing
- AST: Python Abstract Syntax Trees for safe evaluation

## Dataset

The system uses the TMDB 5000 Movie Dataset which includes:
- tmdb_5000_movies.csv
- tmdb_5000_credits.csv

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/Movie-Recommender-System.git
cd Movie-Recommender-System
```

2. Install required packages:
```bash
pip install pandas numpy scikit-learn nltk
```

3. Download required NLTK data:
```python
import nltk
nltk.download('punkt')
```

4. Place the dataset files in the `/dataset` directory:
- `tmdb_5000_movies.csv`
- `tmdb_5000_credits.csv`

## How It Works

1. **Data Processing**:
   - Merges movies and credits data
   - Extracts relevant features (genres, cast, crew, keywords)
   - Processes text data using natural language processing techniques

2. **Feature Engineering**:
   - Combines movie features into tags
   - Applies text stemming for better matching
   - Creates feature vectors using CountVectorizer

3. **Similarity Calculation**:
   - Uses cosine similarity to measure movie relationships
   - Ranks movies based on similarity scores
   - Returns top 5 most similar movies

## Usage

```python
# Import required functions
from movie_recommender import recommend_movie

# Get movie recommendations
recommendations = recommend_movie("Avatar")
print(recommendations)
```

## Example Output

```
Input: "Avatar"
Output:
1. John Carter
2. Aliens
3. Star Trek Into Darkness
4. Ender's Game
5. Pacific Rim
```

## Project Structure

```
Movie-Recommender-System/
├── dataset/
│   ├── tmdb_5000_movies.csv
│   └── tmdb_5000_credits.csv
├── movie_recommender.py
├── requirements.txt
└── README.md
```

## Acknowledgments

- TMDB for providing the movie dataset
- Scikit-learn documentation and community
- NLTK documentation and community