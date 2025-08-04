# Netflix Data Analysis

This project is a comprehensive exploratory data analysis (EDA) of a large movie dataset, with a focus on Netflix-style movie content. The analysis is performed using Python and Jupyter Notebook, leveraging pandas, matplotlib, and seaborn for data manipulation and visualization.

## Dataset

The dataset consists of over 9,800 movies, with the following columns:

- **Release_Date**: The original release date of the movie.
- **Title**: Movie title.
- **Overview**: Brief summary of the movie.
- **Popularity**: A popularity score.
- **Vote_Count**: Number of votes received.
- **Vote_Average**: Average rating (before categorization).
- **Original_Language**: Original language of the movie.
- **Genre**: List of genres.
- **Poster_Url**: URL to the movie’s poster.

After cleaning, unnecessary columns such as `Overview`, `Original_Language`, and `Poster_Url` are dropped to focus on analytical aspects.

## Analysis Workflow

### 1. Data Loading & Initial Exploration

- Importing essential libraries: `numpy`, `pandas`, `matplotlib.pyplot`, `seaborn`.
- Loading the dataset from CSV.
- Viewing data info, checking for duplicates, and exploring column types.

### 2. Data Cleaning & Transformation

- **Release_Date** is converted to `datetime` and then to `year`.
- Dropping unnecessary columns.
- Checking for and dropping any null values.
- The `Genre` column, initially a comma-separated string, is split and exploded to allow per-genre analysis.
- The `Vote_Average` column is categorized into four quartile-based bins: `not_popular`, `below_avg`, `average`, `popular`.

### 3. Feature Engineering

A custom function is defined to categorize numeric columns based on their quartiles, enabling easier visualization and analysis of popularity and ratings.

### 4. Exploratory Data Analysis (EDA) & Visualization

Several key questions are explored:

#### - What is the most frequent genre?
- Used value counts and visualization (seaborn's `catplot`) to display genre distribution.

#### - What is the distribution of movie ratings?
- Visualized the distribution of the categorized `Vote_Average` column.

#### - Which movie is the most popular? What genres does it belong to?
- Identified the movie with the maximum popularity score and listed its genres.

#### - Which movie is the least popular? What genres does it belong to?
- Identified the movie with the minimum popularity score and listed its genres.

### 5. Data Summary

- The data undergoes thorough cleaning: removal of duplicates, handling of missing values, and type casting.
- Genre analysis is performed by exploding multi-genre entries.
- Data is ready for further statistical analysis or machine learning modeling.

## Example Output

**Most Popular Movie:**  
- Title: *Spider-Man: No Way Home*  
- Year: 2021  
- Genres: Action, Adventure, Science Fiction  

**Least Popular Movies:**  
- Titles: *The United States vs. Billie Holiday* (2021), *Threads* (1984)  
- Genres: Music, Drama, History, War, Science Fiction  

## Visualizations

- **Genre Distribution:** Bar plot showing the count of each genre.
- **Vote Average Distribution:** Bar plot of movies per rating category.

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn

## Getting Started

1. Clone this repository.
2. Download the dataset (`mymoviedb.csv`).
3. Open the Jupyter Notebook (`netflix-data-analysis.ipynb`).
4. Run the notebook cells sequentially.

## Usage

The notebook guides you through data cleaning, transformation, and exploratory analysis. You can use the provided code as a template for analyzing other movie datasets or as a foundation for building recommendation systems or advanced analytics.

## License

This project is provided for educational and non-commercial use.

---

*Happy analyzing!*
