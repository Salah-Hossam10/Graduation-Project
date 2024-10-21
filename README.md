# Movie Recommendation System

## Overview

This project is a Movie Recommendation System designed to suggest movies to users based on their preferences. The system utilizes multiple machine learning techniques, including K-Nearest Neighbors (KNN), KD-Tree, and Naive Bayes, to provide personalized movie recommendations. The recommendations are generated based on user ratings, movie genres, and user-defined tags.

## Datasets

The recommendation system is built using the following datasets:

1. **Movies Dataset**: Contains movie titles and genres.
   - Filename: `movies.csv`
2. **Ratings Dataset**: Contains user ratings for movies.
   - Filename: `ratings.csv`
3. **Tags Dataset**: Contains user-defined tags for movies.
   - Filename: `tags.csv`

### Sample Data Structure

#### Movies Dataset
| movieId | title                                 | genres                                 |
|---------|---------------------------------------|----------------------------------------|
| 1       | Toy Story (1995)                     | Adventure|Animation|Children|Comedy|Fantasy |
| 2       | Jumanji (1995)                       | Adventure|Children|Fantasy            |
| ...     | ...                                   | ...                                    |

#### Ratings Dataset
| userId | movieId | rating | timestamp   |
|--------|---------|--------|--------------|
| 1      | 1       | 4.0    | 964982703    |
| 1      | 3       | 4.0    | 964981247    |
| ...    | ...     | ...    | ...          |

#### Tags Dataset
| userId | movieId | tag   | timestamp   |
|--------|---------|-------|--------------|
| 1      | 1       | pixar | 1139045764   |
| 1      | 2       | fun   | 1525286013   |
| ...    | ...     | ...   | ...          |

## Installation

To run this project, you'll need Python and some necessary packages. Follow the steps below to set up your environment:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your_username/your_repository.git
   cd your_repository
Install Required Packages You can install the required packages using pip. It is recommended to create a virtual environment before installing:
bash
Copy code
pip install pandas numpy scipy scikit-learn matplotlib seaborn
Load the Necessary Libraries and Datasets Start by importing the necessary libraries and loading the datasets:

import pandas as pd
import numpy as np
Define Functions to Get Movie Recommendations The following functions are available for getting movie recommendations:

get_movie_recommendation(movie_name): Returns recommendations using KNN.
get_movie_kdtree(movie_name): Returns recommendations using KD-Tree.
get_movie_naiveGaussian(movie_name): Returns recommendations using Naive Bayes.

print("KNN Recommendations:")
print(get_movie_recommendation('Shrek 2'))

KNN Recommendations
Title                                      Distance
1   Shrek (2001)                          0.302120
2   Pirates of the Caribbean: The Curse... 0.333260

print("KDTree Recommendations:")
print(get_movie_kdtree('Shrek 2'))

KDTree Recommendations
Title                                      Distance
1   Ice Age (2002)                        29.406632
2   Men in Black II (2002)                29.782545

print("Naive Bayes Recommendations:")
print(get_movie_naiveGaussian('Shrek 2'))

Naive Bayes Recommendations
Title                                      Distance
1   Shrek (2001)                          0.302120
2   Finding Nemo (2003)                    0.346279

Data Visualization
The project includes various visualizations that help in understanding the datasets and the recommendation system:

Number of Movies per Genre: A bar chart displaying the count of movies across different genres.
Average Rating per Genre: A bar chart showing average ratings for each genre.
Average Rating Over Time: A line plot illustrating how movie ratings have changed over the years.
Heatmap of User Ratings: A heatmap visualizing ratings given by users to sampled movies.

Contributing
Contributions are welcome! If you'd like to contribute to the project, please follow these steps:

Fork the repository.
Create a new branch for your feature or bug fix.
Make your changes and commit them.
Push your changes to your fork.
Submit a pull request detailing your changes.

Acknowledgments
Pandas for data manipulation.
NumPy for numerical operations.
SciPy for scientific computing.
Scikit-learn for machine learning algorithms.
Matplotlib and Seaborn for data visualization.
