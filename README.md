## Netflix Movie Recommendation System 

### Project Overview
This project aims to build a movie recommendation system using machine learning techniques. The system is designed to suggest similar movies based on a given movie's metadata such as cast, crew, keywords, and genres. The project utilizes popular machine learning libraries, including scikit-learn, pandas, and numpy, along with streamlit for a user-friendly web interface.

## Project Structure 

Here is the main structure of the project:

logs/ : Contains log files generated during execution.
mlproject2.egg-info/ : Metadata about the project, typically used during packaging.
notebook/ : Jupyter notebook folder for data exploration and experimentation.
data/ : Dataset and preprocessed files.
tmdb_5000_credits.csv : Dataset containing movie credits information (cast and crew).
tmdb_5000_movies.csv : Dataset with metadata like movie genres and keywords.
movies_dict.pkl : Preprocessed dictionary used for the recommendation engine.
Netflix_Movie_Recommendation.ipynb : Jupyter notebook to test and experiment with the recommendation engine.
similarity.pkl : Pickle file storing the similarity matrix.
src/ : Source code directory containing Python scripts.
pipeline/ : Folder to hold data transformation or modeling pipelines.
__init__.py : Initialization file for the src package.
exception.py : Handles custom exceptions for error handling.
logger.py : Logging setup for tracking events.
utils.py : Utility functions used across the project.
venv/ : Virtual environment containing dependencies for the project.
.gitignore : Specifies files and folders to ignore during Git version control.
app.py : The main Streamlit application file.
README.md : This README file.
requirements.txt : List of all dependencies required for the project.
setup.py : Python setup script for project packaging.


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
