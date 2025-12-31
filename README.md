Task 2 Movie Rating Prediction with Python

This project is part of my CodSoft Data Science Internship (Task 2). The goal is to predict the IMDb rating of Indian movies using basic metadata such as year, duration, genre, and vote count..

Dataset

I used the IMDb India Movies dataset from Kaggle, which contains columns like:

Year
Duration
Genre
Votes
Rating

Only these columns were used in the final model.

Steps Performed

1. Data Loading Loaded the CSV file into a Pandas DataFrame using pd.read_csv with latin1 encoding.

2. Data Cleaning & Preprocessing

Cleaned Year from values like "(2019)" to numeric 2019.

Converted Duration from strings like "109 min" to numeric minutes.

Converted Votes from strings like "1,086" to an integer count.

Ensured Rating was numeric.

Dropped rows with missing values in Year, Duration, Votes, Genre, or Rating.

3. Feature Engineering

Used one-hot encoding (pd.get_dummies) to convert the Genre column into multiple binary features (e.g., Genre_Action. Genre_Comedy, etc.).

4. Model Training

Split the data into training and testing sets (80/20) using train_test_split.

Trained a LinearRegression model to predict Rating from Year, Duration, Votes and Genre dummies.

5. Model Evaluation

Evaluated the model using Mean Absolute Error (MAE) and R² score.

The model achieved: MAE ≈ 1.03 R2≈ 0.09

This means the model's predictions are on average ~1 rating point away from the true IMDb rating and it explains about 9% of the variation in ratings.

Learning Outcomes

From this task I learned:

How to clean messy real-world text data and convert it to numeric form.

How to handle missing values and prepare a clean training dataset.# C
