## Netflix Movie Recommendation System 

### Project Overview
This project aims to build a movie recommendation system using machine learning techniques. The system is designed to suggest similar movies based on a given movie's metadata such as cast, crew, keywords, and genres. The project utilizes popular machine learning libraries, including scikit-learn, pandas, and numpy, along with streamlit for a user-friendly web interface.

## Project Structure 
##    .
##    ├── logs/
##    ├── mlproject2.egg-info/
##    ├── notebook/
##    │   ├── data/
##    │   │   ├── tmdb_5000_credits.csv
##    │   │   ├── tmdb_5000_movies.csv
##    │   │   ├── movies_dict.pkl
##    │   │   ├── Netflix_Movie_Recommendation.ipynb
##    │   │   └── similarity.pkl
##    ├── src/
##    │   ├── __pycache__/
##    │   ├── pipeline/
##    │   ├── __init__.py
##    │   ├── exception.py
##    │   ├── logger.py
##    │   └── utils.py
##    ├── venv/
##    ├── .gitignore
##    ├── app.py
##    ├── README.md
##    ├── requirements.txt
##    └── setup.py

## Key Directories and Files:
notebook/data: Contains the datasets used (tmdb_5000_movies.csv, tmdb_5000_credits.csv), the movie dictionary file (movies_dict.pkl), and a Jupyter notebook for experimentation.
src/: Contains the source code for the project:
logger.py: Handles logging throughout the project.
utils.py: Includes utility functions.
exception.py: Custom exception handling.
pipeline/: Placeholder for your data processing and model pipelines.
app.py: Main application file which runs the recommendation system.
requirements.txt: Lists all necessary libraries for running the project.
.gitignore: Ensures certain files (like large datasets and .pkl files) aren't pushed to version control.

## Dataset
The dataset used in this project is from the TMDb (The Movie Database) API. It includes:

tmdb_5000_credits.csv: Contains information about the cast and crew of movies.
tmdb_5000_movies.csv: Includes metadata such as movie genres, keywords, and production companies.

## Methodology
Data Preprocessing:

Preprocess movie data by extracting relevant features such as genre, director, cast, and keywords.
Use vectorization techniques like CountVectorizer and TF-IDF Vectorizer to convert textual information into numerical representations.
Similarity Calculation:

Using cosine similarity, the project calculates the similarity between movies based on their metadata.
Movie Recommendation:

Based on the similarity matrix, when a user inputs a movie, the system returns the top similar movies.

## Libraries Used
streamlit: For creating the web interface.
pandas: For data manipulation.
numpy: For numerical operations.
scikit-learn: For machine learning tasks like vectorization and similarity computation.
nltk: For natural language processing tasks.
pickle: For saving and loading the movie dictionary and similarity matrix.

## How to Run the Project
Clone the repository :
git clone https://github.com/sarohaanamika/Netflix-Movie-Recommendation-System.git
cd Netflix-Movie-Recommendation-System

Set up a virtual Environment :
python3 -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate

Install Dependencies :
pip install -r requirements.txt

Run the Streamlit APP :
streamlit run app.py


Access the Application: Open your browser and go to http://localhost:8501 to access the recommendation system.
