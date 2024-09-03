# <u>`Hospitality Data Insights and Cancellation Prediction Model`</u>

## Overview

This project focuses on analyzing hospitality data to derive insights and predict hotel booking cancellations. The dataset contains various features related to customer bookings, such as the number of adults, booking changes, arrival date, and more. The primary goal is to build machine learning models that can accurately predict whether a booking will be canceled.

## Table of Contents
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Results](#results)

## Dataset

The dataset used in this project includes the following features:

- `hotel`: Type of hotel (Resort Hotel or City Hotel)
- `is_canceled`: Indicates if the booking was canceled (1) or not (0)
- `lead_time`: Number of days between the booking date and the arrival date
- `arrival_date_year`: Year of arrival date
- `arrival_date_month`: Month of arrival date
- `arrival_date_week_number`: Week number of year for arrival date
- `arrival_date_day_of_month`: Day of the month of arrival date
- `stays_in_weekend_nights`: Number of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel
- `stays_in_week_nights`: Number of weeknights (Monday to Friday) the guest stayed or booked to stay at the hotel
- `adults`: Number of adults
- `children`: Number of children
- `babies`: Number of babies
- `meal`: Type of meal booked
- `country`: Country of origin of the customer
- `market_segment`: Market segment designation
- `distribution_channel`: Booking distribution channel
- `is_repeated_guest`: Whether the guest is a repeated guest or not
- `previous_cancellations`: Number of previous bookings that were canceled by the customer
- `previous_bookings_not_canceled`: Number of previous bookings not canceled by the customer
- `reserved_room_type`: Code of room type reserved
- `assigned_room_type`: Code for the room type assigned
- `booking_changes`: Number of changes made to the booking
- `deposit_type`: Type of deposit made for the booking
- `agent`: ID of the travel agency that made the booking
- `company`: ID of the company that made the booking
- `days_in_waiting_list`: Number of days the booking was in the waiting list
- `customer_type`: Type of customer, assuming one of four categories
- `adr`: Average Daily Rate, calculated by dividing the sum of all lodging transactions by the total number of staying nights
- `required_car_parking_spaces`: Number of car parking spaces required by the customer
- `total_of_special_requests`: Number of special requests made by the customer
- `reservation_status`: Reservation last status, assuming one of three categories
- `reservation_status_date`: Date at which the last status was set
- `guest_category`: Categorized guest based on criteria
- `lead_time_category`: Lead time categorized for easier analysis

## Data Preprocessing

Data preprocessing steps include:

1. **Handling Missing Values:** Missing data was managed through imputation or removal, depending on the feature.
2. **Encoding Categorical Variables:** Categorical variables were converted to numeric using Label Encoding.
3. **Feature Scaling:** Numeric features were scaled using `StandardScaler` to ensure that all features contribute equally to the model.
4. **Class Imbalance Handling:** The dataset showed a class imbalance in the `is_canceled` target variable, which was addressed using SMOTE (Synthetic Minority Over-sampling Technique).

## Exploratory Data Analysis

Exploratory Data Analysis (EDA) was conducted to understand the distribution of features, correlations between features, and their relationship with the target variable `is_canceled`. Key insights were visualized using various plots.

## Feature Engineering

Feature engineering involved the creation of new features such as:

- `guest_category`: Based on guest behavior and booking patterns.
- `lead_time_category`: Categorized the `lead_time` into bins.

## Modeling

Several machine learning models were trained and evaluated:

1. **Random Forest Classifier**
2. **Logistic Regression**
4. **Decision Tree Classifier**

Hyperparameter tuning was performed using `GridSearchCV` to find the best model configurations.

## Evaluation

The models were evaluated using the following metrics:

- **Accuracy:** The overall accuracy of the model.
- **Precision:** The precision score of the model.
- **Recall:** The recall score of the model.
- **F1 Score:** The harmonic mean of precision and recall.
- **Confusion Matrix:** To visualize the performance of the model in predicting true positives, false positives, true negatives, and false negatives.

## Results

The models were compared based on the evaluation metrics. The Logistic Regression model performed the best with the highest F1 score and accuracy. The confusion matrix showed a strong ability to predict cancellations accurately.

## Conclusion

This project successfully demonstrated how machine learning models can predict hotel booking cancellations with high accuracy. The Logistic Regression model was the most effective, but the Logistic Regression and Decision Tree models also provided valuable insights. Future improvements could include feature importance analysis and deploying the model for real-time prediction.

## Installation

- Clone the repository:
   ```bash
   git clone https://github.com/ajitmane36/hospitality-data-insights-and-cancellation-prediction-model.git
