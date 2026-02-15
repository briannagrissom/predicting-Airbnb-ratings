# San Francisco Airbnb Ratings Prediction

This project focuses on predicting the average rating for Airbnb listings in San Francisco using data from December 2023. The goal is to build regression models that accurately estimate ratings and to identify which specific listing features—such as price, host behavior, and amenities—significantly influence guest experiences.

## Project Overview

The dataset contains over 6,000 observations of Airbnb listings. Since ratings are continuous values ranging from 1 to 5 stars, this is treated as a regression problem. The project explores various machine learning algorithms to determine which factors contribute most to high star ratings.

### Data Source

The listing data was sourced from Inside Airbnb, specifically the San Francisco dataset updated in late 2023.

### Features and Preprocessing
The raw data was cleaned and transformed to improve model performance:

Feature Engineering: Created new indicators such as "Days as Host," "Number of Amenities," and whether the host lives locally in San Francisco.

Data Cleaning: Dropped irrelevant metadata columns (e.g., URLs, descriptions) and focused on listing-specific attributes.

Imputation: Missing values for numerical features like beds, host_response_rate, and reviews_per_month were handled using a K-Nearest Neighbors (KNN) imputer.

Exploratory Data Analysis: Analyzed the distribution of reviews, which showed a strong skew toward 5-star ratings, evaluated the impact of price bins on median ratings, and explored how various feature varibles correlated with customer rating.

### Models Explored

The following regression models were implemented and compared:

Random Forest Regressor to capture non-linear relationships, Linear Regression for a standard baseline, Support Vector Regression to explore high-dimensional spaces, and Gradient Boosting Regressor to explore sequentially-made trees.


### Key Insights

Host Experience: The most significant predictors of ratings were found to be the host's total listing count and the number of private rooms they manage. This suggests that more experienced hosts tend to receive better reviews.

Price and Stability: Higher-priced listings generally receive higher and more stable (lower variance) ratings.

Model Limitations: Due to the heavily skewed distribution of reviews (most being near 5.0), models tended to overpredict for lower-rated listings. Future improvements would benefit from a more even distribution of rating data.
