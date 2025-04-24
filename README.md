# Movie Rating Prediction Project

## Overview
This project aims to predict movie ratings based on various features such as year of release, duration, votes, genre, director, actors, and derived metrics like director success rate and genre average rating. The project uses a Random Forest Regressor model for prediction and evaluates its performance using standard regression metrics.

## Dataset
The dataset used is "IMDb Movies India.csv", which contains information about Indian movies listed on IMDb. The dataset includes features like:
- Name
- Year
- Duration
- Genre
- Rating
- Votes
- Director
- Actor 1, Actor 2, Actor 3

## Data Preprocessing
1. **Handling Missing Values**:
   - Rows with missing ratings were dropped
   - Missing values in categorical columns (Genre, Director, Actors) were filled with 'Unknown'
   - Missing durations were filled with the median duration
   - Missing years were filled with the mode year

2. **Feature Engineering**:
   - Extracted numerical values from 'Duration' (removing text)
   - Cleaned 'Votes' by removing commas and converting to numeric
   - Extracted year from strings in 'Year' column
   - Created new features:
     - Director_Success_Rate: Average rating of movies by each director
     - Genre_Avg_Rating: Average rating for each genre

3. **Encoding**:
   - Used Label Encoding for categorical variables (Genre, Director, Actors)

## Model Training
- **Algorithm**: Random Forest Regressor
- **Parameters**: n_estimators=100, random_state=42
- **Train-Test Split**: 80-20 split with random_state=42

## Evaluation Metrics
The model was evaluated using:
1. Mean Absolute Error (MAE): 0.5455
2. Root Mean Squared Error (RMSE): 0.7785
3. R² Score: 0.6740

## Requirements
To run this project, you'll need:
- Python 3.x
- pandas
- numpy
- scikit-learn

## How to Run
1. Clone the repository
2. Install the required packages: `pip install pandas numpy scikit-learn`
3. Ensure the dataset "IMDb Movies India.csv" is in the same directory
4. Run the Jupyter notebook or convert it to a Python script and execute it

## Future Improvements
1. Try different regression models (e.g., Gradient Boosting, Neural Networks)
2. Perform more extensive feature engineering
3. Implement hyperparameter tuning for better performance
4. Add more features if available (e.g., budget, production house)

## Author
Makhan Yadav

## Acknowledgments
- IMDb for providing the dataset
- Scikit-learn for the machine learning algorithms
- Python community for the open-source libraries