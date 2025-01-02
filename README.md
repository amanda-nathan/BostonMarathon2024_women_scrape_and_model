# Boston Marathon 2024 Women’s Scraping & Prediction Model

This project demonstrates how to scrape data from the 2024 Boston Marathon Women's results and predict marathon finish times based on half marathon times. The project uses machine learning models such as **Random Forest** (Bagging) and **Gradient Boosting** (Boosting) to make predictions.

## Table of Contents

- [Project Overview](#project-overview)
- [Data Scraping](#data-scraping)
- [Prediction Model](#prediction-model)
- [Evaluation](#evaluation)
- [Future Improvements](#future-improvements)
- [Installation and Usage](#installation-and-usage)
- [Contributors](#contributors)

## Project Overview

This repository includes a Python notebook where:
- **Data** from the 2024 Boston Marathon Women's results was scraped and cleaned.
- Two machine learning models (Random Forest and Gradient Boosting) were trained to predict **Finish Net time** based on the **Half marathon time**.
- The project compares the performance of these models and evaluates them using **Mean Absolute Error (MAE)** and **Mean Squared Error (MSE)**.

## Data Scraping

The data for this project was scraped directly from the Boston Marathon website:  
[https://results.baa.org/2024/](https://results.baa.org/2024/)

The data scraping process involves:
- Retrieving individual marathon result data (including place, name, gender, bib, and timing information).
- Cleaning the data to remove irrelevant information and format time fields.
- Storing the cleaned data in a CSV file for further analysis.

## Prediction Model

### Machine Learning Models Used:
- **Random Forest (Bagging)**: A robust ensemble model that builds multiple decision trees and averages their predictions to improve accuracy.
- **Gradient Boosting (Boosting)**: Another ensemble method, but it builds trees sequentially, with each tree attempting to correct the errors of the previous one.

### Input:
- **Half marathon time** in minutes.

### Output:
- **Predicted Finish Net time** (time to finish the full marathon from start).

## Evaluation

The models were evaluated using:
- **Mean Absolute Error (MAE)**: Measures the average magnitude of errors in predictions.
- **Mean Squared Error (MSE)**: Measures the average of the squared differences between predicted and actual values.

### Results:
- Random Forest Model achieved a **MAE** of 9.95 minutes and an **MSE** of 194.77 minutes².
- Gradient Boosting Model achieved a **MAE** of 8.60 minutes and an **MSE** of 145.47 minutes².

After hyperparameter tuning:
- Random Forest tuned model achieved a **MAE** of 8.87 minutes and an **MSE** of 156.28 minutes².
- Gradient Boosting tuned model achieved a **MAE** of 8.48 minutes and an **MSE** of 143.18 minutes².

## Future Improvements

- **Stratification by age**: A more granular approach would involve stratifying the data by age and other relevant variables. This would provide more accurate predictions tailored to different age groups.
- **More sophisticated feature engineering**: Incorporating more factors such as weather, race conditions, or experience could improve model accuracy.
- **Additional modeling approaches**: Explore other algorithms like XGBoost, LightGBM, or Neural Networks for better performance.

## Installation and Usage

### Dependencies:
To run this project, you will need the following libraries:

- `pandas`
- `numpy`
- `scikit-learn`
- `seaborn`
- `matplotlib`
- `requests` (for scraping)

To install the dependencies, you can run:

```bash
pip install -r requirements.txt
