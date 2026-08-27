# Iris Flower Classification 🌸

A beginner-friendly **Machine Learning classification project** that predicts the species of an Iris flower using its sepal and petal measurements.

The project uses a **Random Forest Classifier** from Scikit-learn and demonstrates the basic workflow of loading data, separating features and target, training a model, and making predictions.

## 📌 Project Overview

The goal of this project is to classify Iris flowers into their respective species based on four measurements:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

The target variable is the Iris flower species:

* `Iris-setosa`
* `Iris-versicolor`
* `Iris-virginica`

## 🧠 Machine Learning Model

### Random Forest Classifier

The project uses:

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier()
```

The model is trained using the four flower measurements as input features and the `Class` column as the target.

## 📂 Project Structure

```text
Iris/
│
├── iris.ipynb
├── iris_train.csv
├── iris_test.csv
└── README.md
```

### Files

| File             | Description                                            |
| ---------------- | ------------------------------------------------------ |
| `iris.ipynb`     | Jupyter Notebook containing the complete ML workflow   |
| `iris_train.csv` | Training dataset used to train the Random Forest model |
| `iris_test.csv`  | Test dataset used for generating predictions           |
| `README.md`      | Project documentation                                  |

## 📊 Dataset

The training dataset contains four numerical features and one target column:

| Feature      | Description         |
| ------------ | ------------------- |
| Sepal length | Length of the sepal |
| Sepal width  | Width of the sepal  |
| Petal length | Length of the petal |
| Petal width  | Width of the petal  |
| Class        | Target Iris species |

The training data contains **124 samples** and **4 input features**.

## 🔄 Workflow

The project follows these steps:

```text
Load Training Data
       ↓
Separate Features (X) and Target (y)
       ↓
Create Random Forest Classifier
       ↓
Train the Model
       ↓
Load Test Data
       ↓
Separate Test Features
       ↓
Generate Predictions
```

### 1. Load the training data

```python
data = pd.read_csv("iris_train.csv")
```

### 2. Separate features and target

```python
x = data.iloc[:, :-1]
y = data.iloc[:, -1]
```

The four measurement columns are used as features, while `Class` is used as the target.

### 3. Create and train the model

```python
model = RandomForestClassifier()
model.fit(x, y)
```

### 4. Make a prediction

For example, the model was given:

```text
[5.4, 3.9, 1.7, 0.4]
```

and predicted:

```text
Iris-setosa
```

### 5. Predict on the test dataset

The test features are passed to the trained model:

```python
predictions = model.predict(x_test.values)
```

## 🛠️ Technologies Used

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook
* Random Forest Classification

## 💻 Installation

Clone the repository:

```bash
git clone <your-repository-url>
```

Move into the project folder:

```bash
cd Iris
```

Install the required libraries:

```bash
pip install pandas scikit-learn jupyter
```

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
iris.ipynb
```

## 🚀 How to Run

1. Keep `iris.ipynb`, `iris_train.csv`, and `iris_test.csv` in the same folder.
2. Open `iris.ipynb` in Jupyter Notebook.
3. Run the cells in order.
4. The Random Forest model will be trained using `iris_train.csv`.
5. The trained model will then generate predictions for the test data.

## 📈 Example Prediction

**Input:**

```text
Sepal length = 5.4
Sepal width  = 3.9
Petal length = 1.7
Petal width  = 0.4
```

**Prediction:**

```text
Iris-setosa
```

## 🎯 Learning Objectives

Through this project, I practiced:

* Loading datasets using Pandas
* Understanding features and target variables
* Preparing data for machine learning
* Using a classification algorithm
* Training a Random Forest model
* Making predictions on new data
* Working with CSV datasets
* Using Scikit-learn for machine learning

## 🔮 Future Improvements

Possible improvements for this project include:

* Add train/test evaluation metrics such as accuracy
* Generate a confusion matrix
* Compare Random Forest with other classification algorithms
* Add data visualization
* Use a Scikit-learn Pipeline for preprocessing and modeling
* Improve the notebook structure and documentation

## 👨‍💻 Author

**Gaurav Yadav**

This project was created as part of my Machine Learning learning journey.