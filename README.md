# Hair Salon Appointment Management System

This project focuses on the development of a web-based application for managing hair salon appointments.

A machine learning model was designed and trained using a custom dataset in order to learn patterns in customer behavior
and predict arrival status based on the type of service.

The dataset was designed specificly for this purpose and supports the training and evaluation of the model.

## About the dataset

The dataset consists of 200 entries collected between **January 1st, 2026** and **March 27, 2026**.
Days off/(national) holidays excluded.

It consists of the following columns:

- ID
- Date and time *(in one column)*
- Service type *(dye, haircut, treatment)*
- Duration *(in minutes)*
- Number of total visits
- Days since last visit
- Arrival status *(on time, late, no show)*
- Waiting time *(in minutes)*

## Project requirements

This project is fully implemented in Python using Jupyter Notebook.

All required libraries are listed in the Packages sub-section, under the Implementation section.

## Implementation
### Packages

The model was implemented in Jupyter Notebook, using the following Python packages/libraries:

### Core packages

- scikit-learn
- pandas

### Sub-packages (packages used for data preprocessing and model deployment)

Classifiers, evaluation metrics (when necessary) and train-test splitting have been implemented using the `scikit-learn` library,
was used as the core library for model development, including preprocessing, model training, and evaluation utilities.

### Classifiers

The model was trained using the Random Forest classifier from the scikit-learn `ensemble` module.

    from sklearn.ensemble import RandomForestClassifier

### Evaluation metrics (when necessary)

Model performance was evaluated using standard classification metrics.
Additional evaluation was performed using a confusion matrix and classification report from the scikit-learn `metrics` module.

#### Accuracy

    from sklearn.metrics import accuracy_score

#### Precision

    from sklearn.metrics import precision_score

#### Recall

    from sklearn.metrics import recall_score

#### F1-score

    from sklearn.metrics import f1_score

#### Confusion matrix

    from sklearn.metrics import confusion_matrix

#### Classification report

    from sklearn.metrics import classification_report

### Train-test splitting

Train-test split has been performed using the `model_selection` module of the scikit-learn Python library.

    from sklearn.model_selection import train_test_split

### Model export

The trained machine learning model was exported using the joblib library in Python and stored in a `.pkl` file format.

This enables model reuse and allows easy loading and deployment without further retraining.

**IMPORTANT:** The model can later be loaded and deployed using `joblib.load()`.

## Running the project

Before proceeding with the main steps, make sure you download the following files included in the project repository.

- HairSalonData.csv
- HairSalonModel.ipynb

After downloading both the `.csv` and `.ipynb` files required, create a new folder (preferably in Desktop, Documents is also a reliable option)
where both files will be stored, as well as generated models when running the Jupyter Notebook script.

**IMPORTANT:** To ensure proper functionality, move the `.csv` and `.ipynb` files into the newly created folder.

Before starting, ensure that all files have been downloaded.

### Option 1: Jupyter Notebook (recommended)

Start Jupyter Notebook by running:

    jupyter notebook

into your terminal.

Open the provided `.ipynb` file from the browser interface (localhost:8888), navigating into the directory where it is stored.

Run all cells sequentially to execute the full pipeline.

### Option 2: VS Code

Open the project folder in Visual Studio Code.

Open the .ipynb file, stored in the project folder, using the Jupyter extension.

Run all cells sequentially.