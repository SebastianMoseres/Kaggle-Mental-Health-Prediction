# Predicting Mental Health Status from Survey Data

## Project Overview

This project uses a synthetic dataset from a [Kaggle Playground Series competition (S4E11)](https://www.kaggle.com/competitions/playground-series-s4e11) to build a machine learning model that predicts the likelihood of depression based on survey responses.

The project demonstrates a complete end-to-end data science workflow, from initial data exploration and cleaning to model training, evaluation, and final prediction. A Keras Neural Network was found to be the best-performing model with a validation accuracy of **94.64%**.

---

## Workflow

1.  **Exploratory Data Analysis (EDA):** Investigated feature distributions, correlations, and identified a structural pattern in missing data related to user occupation (Student vs. Working Professional).

2.  **Data Preprocessing:**
    *   Cleaned column names and dropped irrelevant features (`id`, `Name`).
    *   Strategically filled missing values based on the user's occupation.
    *   One-hot encoded all categorical features to prepare the data for machine learning models.

3.  **Model Training & Validation:**
    *   Four different models were trained and evaluated on a validation set (20% of the training data):
        *   Logistic Regression (Baseline)
        *   Random Forest
        *   LightGBM
        *   Keras Neural Network
    *   All models were evaluated using the accuracy metric.

4.  **Model Selection & Final Prediction:**
    *   The Neural Network achieved the highest validation accuracy and was selected as the final model.
    *   The model was then trained on the full dataset and used to generate predictions on the official competition test set.

---

## Results

The models' performance on the validation set was as follows:

| Model               | Validation Accuracy |
| ------------------- | ------------------- |
| **Neural Network**  | **0.9464**          |
| LightGBM            | 0.9388              |
| Logistic Regression | 0.9380              |
| Random Forest       | 0.9341              |

---

## How to Run

1.  Clone this repository:
    ```bash
    git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git
    ```
2.  Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open and run the `Mental_Health_Analysis.ipynb` notebook in a Jupyter environment.

**Note:** The dataset is not included in this repository. It must be downloaded from the [Kaggle competition page](https://www.kaggle.com/competitions/playground-series-s4e11/data) and placed in the root directory.

---