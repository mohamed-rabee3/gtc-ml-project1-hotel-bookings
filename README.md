
# Hotel Booking Analysis & Cancellation Prediction

This project provides a comprehensive analysis of hotel booking data. It involves data cleaning, exploratory data analysis (EDA), and preparation for building a machine learning model to predict booking cancellations. The entire workflow is documented in the Jupyter Notebook `hotel_booking_data_cleaning.ipynb`.

-----

## 📋 Table of Contents

  * [Overview](https://www.google.com/search?q=%23-overview)
  * [Dataset](https://www.google.com/search?q=%23-dataset)
  * [Dependencies](https://www.google.com/search?q=%23-dependencies)
  * [Workflow](https://www.google.com/search?q=%23-workflow)
  * [Data Cleaning & Preprocessing](https://www.google.com/search?q=%23-data-cleaning--preprocessing)
  * [Exploratory Data Analysis (EDA)](https://www.google.com/search?q=%23-exploratory-data-analysis-eda)
  * [Feature Engineering](https://www.google.com/search?q=%23-feature-engineering)
  * [Model Preparation](https://www.google.com/search?q=%23-model-preparation)
  * [How to Run](https://www.google.com/search?q=%23-how-to-run)

-----

## 📝 Overview

The primary objective of this project is to analyze a hotel booking dataset to uncover insights and patterns. The notebook walks through the essential steps of a data science project, starting from data loading and cleaning, moving to in-depth exploratory analysis, and finally preparing the data for predictive modeling. The end goal is to build a model that can accurately predict whether a booking will be canceled.

-----

## 💾 Dataset

The dataset contains booking information for a city hotel and a resort hotel. It includes a rich set of features that provide details about each booking, such as:

  * **Booking Information**: `hotel`, `is_canceled`, `lead_time`, `arrival_date_year`, `arrival_date_month`, `arrival_date_week_number`, `arrival_date_day_of_month`.
  * **Guest Information**: `adults`, `children`, `babies`, `country`.
  * **Booking Details**: `meal`, `market_segment`, `distribution_channel`, `is_repeated_guest`, `previous_cancellations`, `previous_bookings_not_canceled`, `reserved_room_type`, `assigned_room_type`, `booking_changes`, `deposit_type`, `agent`, `company`, `days_in_waiting_list`, `customer_type`, `adr`, `required_car_parking_spaces`, `total_of_special_requests`.

-----

## 🛠️ Dependencies

To run the notebook, you need Python 3 and the following libraries:

  * **`pandas`**: For data manipulation and analysis.
  * **`numpy`**: For numerical operations.
  * **`matplotlib`**: For creating static, animated, and interactive visualizations.
  * **`seaborn`**: For making attractive and informative statistical graphics.
  * **`scikit-learn`**: For machine learning tools, including data splitting.

You can install these dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

-----

## 🔄 Workflow

The project follows a structured data analysis workflow:

1.  **Environment Setup**: Importing necessary libraries and setting a random seed for reproducibility.
2.  **Data Loading**: Loading the dataset from a CSV file into a pandas DataFrame.
3.  **Initial Exploration**: Performing a preliminary check of the data's structure, data types, and summary statistics.
4.  **Data Cleaning**: (Although not explicitly detailed in the provided notebook, this step would typically involve handling missing values, correcting data types, and removing duplicates).
5.  **Univariate EDA**: Analyzing individual features (both continuous and categorical) to understand their distributions and characteristics.
6.  **Feature Separation**: Classifying columns as either continuous or categorical for targeted preprocessing.
7.  **Data Splitting**: Dividing the dataset into training and testing sets to prepare for model building.

-----

## 🧼 Data Cleaning & Preprocessing

The initial steps focus on preparing the data for analysis. This involves:

  * **Loading the data** into a pandas DataFrame.
  * **Initial Inspection** using `df.info()`, `df.describe()`, and `df.head()` to get a first look at the data's integrity and content.

-----

## 📊 Exploratory Data Analysis (EDA)

A thorough univariate analysis is conducted to understand each feature individually.

### Continuous Features

For numerical columns, the following analyses are performed:

  * **Descriptive Statistics**: Calculating `mean`, `median`, `std`, and `skewness`.
  * **Visualization**:
      * **Histograms and KDE plots** are used to visualize the distribution of each variable.
      * **Boxplots** are used to identify the spread, central tendency, and potential outliers.

### Categorical Features

For categorical columns, the analysis includes:

  * **Cardinality Check**: Counting the number of unique values in each column.
  * **Frequency Analysis**: Displaying the top categories by count and percentage.
  * **Visualization**: Using **bar plots** to show the frequency distribution of categories.

-----

## ✨ Feature Engineering

Based on the EDA, the features are segregated to streamline further processing:

  * **`continuous_cols`**: A list of columns identified as continuous variables.
  * **`categorical_cols`**: A list of columns identified as categorical variables.

This separation is crucial for applying appropriate encoding techniques (e.g., one-hot encoding for categorical data) and scaling methods (e.g., standardization for continuous data) before model training.

-----

## 🤖 Model Preparation

The final step in the notebook is preparing the data for machine learning.

  * The target variable `is_canceled` is separated from the feature set.
  * The dataset is split into training (80%) and testing (20%) sets using `train_test_split` from `scikit-learn`. This ensures that the model is trained on one subset of the data and evaluated on a separate, unseen subset.

