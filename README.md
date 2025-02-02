---

# Phishing Website Detection with Logistic Regression

This project uses machine learning techniques to classify URLs as phishing or legitimate websites. The model is trained using features derived from URLs, such as length, number of dots, and the presence of certain characters. The goal is to identify phishing websites based on these features.

## Prerequisites

Make sure you have the following installed:

-   Python 3.x
-   Jupyter Notebook
-   pip

### Install Dependencies

You can install the necessary dependencies using the following command:

```bash
pip install pandas scikit-learn
```

### Jupyter Notebook Setup

If you don't have Jupyter Notebook installed, you can install it with the following command:

```bash
pip install notebook
```

Then, start Jupyter Notebook with:

```bash
jupyter notebook
```

## Dataset

The dataset used in this project is available on Kaggle. You can download it using the link below:

-   [Phishing Dataset for Machine Learning](https://www.kaggle.com/datasets/shashwatwork/phishing-dataset-for-machine-learning)

After downloading, unzip the dataset and place the `phishing.csv` file in a folder called `phishing_data/` within your project directory.

## How to Run

1. Open Jupyter Notebook by running the following command in your terminal:

```bash
jupyter notebook --ip=0.0.0.0 --no-browser --allow-root --NotebookApp.token=''
```

2. Open the `phishing_detection.ipynb` notebook.
3. Run the cells in the notebook sequentially to train the model and evaluate its performance.

## Script Overview

The notebook performs the following steps:

1. **Load the dataset** using `pandas`.
2. **Feature Selection**: Selects relevant features (e.g., `UrlLength`, `NumDots`, etc.).
3. **Train-Test Split**: Divides the dataset into training and testing sets.
4. **Feature Scaling**: Normalizes the data using `StandardScaler` for better performance.
5. **Model Training**: A Logistic Regression model is trained on the dataset.
6. **Evaluation**: The model is evaluated on the test set, and accuracy along with a classification report are printed.

## Output

The notebook will output:

-   Model accuracy
-   Classification report including precision, recall, F1-score for both classes (phishing and legitimate websites)

Example output:

```bash
模型准确率: 64.35%

分类报告:
              precision    recall  f1-score   support

           0       0.62      0.70      0.66       988
           1       0.67      0.58      0.62      1012

   accuracy                            0.64      2000
   macro avg       0.65      0.64      0.64      2000
weighted avg       0.65      0.64      0.64      2000
```

## Future Work

-   Experiment with more sophisticated models (e.g., Random Forest, XGBoost).
-   Use additional features and/or pre-processing techniques for better performance.
-   Integrate with a real-time URL scanner for phishing detection in browsers.

---
