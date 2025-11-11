# Stroke Prediction using Machine Learning

## Overview
This project uses **scikit-learn** and several different machine learning models to predict whether a patient is at high risk of having a stroke. Identifying high-risk individuals can help doctors provide better guidance to patients and their families on how to respond in case of an emergency.

### Dataset
The dataset used for this analysis is the [Stroke Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) from Kaggle.

#### Data Overview
| Column              | Non-Null Count | Dtype    |
|---------------------|----------------|----------|
| id                  | 5110           | int64    |
| gender              | 5110           | object   |
| age                 | 5110           | float64  |
| hypertension        | 5110           | int64    |
| heart_disease       | 5110           | int64    |
| ever_married        | 5110           | object   |
| work_type           | 5110           | object   |
| Residence_type      | 5110           | object   |
| avg_glucose_level   | 5110           | float64  |
| bmi                 | 4909           | float64  |
| smoking_status      | 5110           | object   |
| stroke              | 5110           | int64    |

## Model Selection and Findings
Since false negatives (failing to identify a high-risk patient) are more critical than false positives, the best model for this application is likely **Voting Classifier (SMOTE)** or **XGB (GridSearchCV)**.

## Areas for Improvement
This analysis could be enhanced by:
- Further **outlier handling**
- **Feature engineering** to improve model performance
- **Collecting more data** on stroke patients to address class imbalance
- Exploring **ensemble models** or different algorithms
- Implementing **cross-validation** for robustness

## Setup Instructions
To replicate this project, follow the steps below:

### 1. Clone the Repository
```bash
git clone https://github.com/your-repo/stroke-prediction.git
cd stroke-prediction
```

### 2. Set Up the Environment
This project uses Conda for package management. To create and activate the environment, run:
```bash
conda env create -f environment.yml
conda activate stroke-prediction
```

### 3. Install Additional Dependencies (if needed)
If you need to install additional packages, you can do so using pip:
```bash
pip install -r requirements.txt
```

### 4. Run the Jupyter Notebook
Launch Jupyter Notebook and open the project:
```bash
jupyter notebook
```

## 🚀 Deployment

To run the project as a server, use:

```bash
python server.py
```

Make sure you have completed the following setup:

- You are in the root directory where `server.py` is located.
- All dependencies are installed. If not, run:

  ```bash
  pip install -r requirements.txt
  ```

- If applicable, ensure any environment variables or config files (like `.env`) are properly set up.

After running `server.py`, the terminal will indicate the server URL (e.g., `http://localhost:5000`).  
To access the front end, **append `/docs` to the URL**:

```
http://localhost:5000/docs
```

This will open the interactive front-end interface powered by FastAPI.

## 🗂 Project Structure

```
├── data/               # Dataset files
├── notebooks/          # Jupyter notebooks
├── models/             # Saved models
├── server.py           # Deployment script
├── environment.yml     # Conda environment definition
├── requirements.txt    # Pip dependencies
└── README.md           # Project documentation
```

## License
This project is licensed under the MIT License.
