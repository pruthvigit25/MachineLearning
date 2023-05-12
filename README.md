# Airbnb Rating Prediction Project

This project aims to predict the ratings associated with Airbnb listings in Dublin, Leinster, Ireland. The goal is to build predictive models using text and numeric features to accurately predict the ratings for each listing.

## Dataset

The project utilizes two datasets:

1. `listings.csv`: Contains property details and ratings.
2. `reviews.csv`: Contains text reviews for each listing.

## Exploratory Data Analysis

During the exploratory analysis, several important findings were made:

1. The dataset exhibited a high degree of class imbalance, with the majority of ratings falling into the 5-star category, followed by 4-star ratings. This imbalance poses a challenge for modeling.
2. Null values were present in the rating columns, with the highest number of null values observed in `review_scores_rating`.
3. The correlation analysis revealed that no single independent variable had a strong correlation with the predicted variables.
4. The number of reviews varied significantly between low-rating listings and high-rating listings, with high-rating listings generally having more reviews.

## Predictive Models

Two types of models were built to predict the ratings:

1. Text Feature-based Model:
   - Algorithms used: Naïve Bayes, Logistic Regression, Random Forest, SVM, CatBoost
   - Best performing algorithm on training dataset: Logistic Regression (Accuracy: 0.9974, Balanced Accuracy: 0.9928)
   - Best performing algorithm on test dataset: Random Forest (Accuracy: 0.8449, Balanced Accuracy: 0.5294)

2. Numeric Feature-based Model:
   - Algorithms used: KNN, Random Forest, SVM, CatBoost, xgBoost
   - Best performing algorithm on training dataset: CatBoost (Accuracy: 0.9686, Balanced Accuracy: 0.9549)
   - Best performing algorithm on test dataset: CatBoost (Accuracy: 0.8111, Balanced Accuracy: 0.3553)

## Results

The evaluation of the predictive models yielded the following results:

### Text Feature-based Model:

| Algorithm           | Accuracy | Balanced Accuracy |
|---------------------|----------|-------------------|
| Naïve Bayes         | 0.8558   | 0.4529            |
| Logistic Regression | 0.9974   | 0.9928            |
| Random Forest       | 0.7269   | 0.8020            |
| SVM                 | 0.9399   | 0.8743            |
| CatBoost            | 0.9065   | 0.5361            |

### Numeric Feature-based Model:

| Algorithm           | Accuracy | Balanced Accuracy |
|---------------------|----------|-------------------|
| KNN                 | 0.6371   | 0.1826            |
| Random Forest       | 0.8118   | 0.3193            |
| SVM                 | 0.6330   | 0.1702            |
| CatBoost            | 0.9686   | 0.9549            |
| xgBoost             | 0.8118   | 0.3193            |


