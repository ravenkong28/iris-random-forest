# 🌸 Iris Flower Classification – Random Forest

This project predicts species of iris flowers based on flower measurements using **Random Forest Classifier**. Both **RapidMiner** and **Python** implementations were compared.

## 📌 Objective
Build a multi-class classification model for the Iris dataset using Random Forest and compare performance between Python and RapidMiner tools.

## 🌱 Dataset Overview
- Samples: 150
- Classes: `Iris-setosa`, `Iris-versicolor`, `Iris-virginica`
- Features:
  - Sepal Length
  - Sepal Width
  - Petal Length
  - Petal Width

## 🧪 Tools & Libraries
- **RapidMiner Studio**
- **Python 3**, Jupyter Notebook
- Libraries: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`

## ⚙️ Methodology

### 📌 RapidMiner Workflow
![Gambar1 - Overall Process Design](/images/Gambar1.png)

Inside the Cross Validation process, the Random Forest model is trained and tested using 10-fold cross-validation.
![Gambar1.1 - Cross Validation Details with Random Forest](/images/Gambar1.1.png)

### 📌 Python Approach
- Data split into training and testing sets
- RandomForestClassifier from `scikit-learn` used for training
- Evaluation via confusion matrix and classification report
- Feature importance visualized

## 📊 Results
### 📈 RapidMiner Results
![Gambar2 - RapidMiner Accuracy & Confusion Matrix](/images/Gambar2.png)

- Accuracy: **96.00% ± 4.66%**
- Very balanced performance across all classes

### 🐍 Python Results

#### 🔍 Classification Report
![Gambar3 - Python Classification Report](/images/Gambar3.png)

- Accuracy: **100%** on test set
- Perfect precision, recall, and F1-score for all classes

#### 🔁 Cross Validation Accuracy (Python)
![Gambar4 - Cross Validation Accuracy in Python](/images/Gambar4.png)

Cross-Validation Accuracy: 96.67% ± 2.11%

**Cross-Validation vs. Single Train-Test Split**:
- Cross-validation resulted in an average accuracy of 96.67% ± 2.11%, which is more realistic for measuring model performance.
- The previous single train-test split achieved 100% accuracy, but this could be due to the coincidence of the test data split, which is easy to classify.
- Cross-validation is more reliable because it takes the average of various data split scenarios, so the results are more stable and generalized.


#### 🧠 Feature Importance
![Gambar5 - Feature Importance Python](/images/Gambar5.png)

- Features a3 and a4 have the most influence on classification, while a2 contributes almost nothing.
- This can be used for feature selection, if you want to simplify the model without losing accuracy.

## ✅ Conclusion
| Platform     | Accuracy |
|--------------|----------|
| RapidMiner   | ~96%     |
| Python       | ~100%               |
| Python(CV)   | ~96.67% ± 2.11%%    |

- Random Forest performed excellently on both platforms
- Python provides more flexibility for fine-tuning and visualizations
- RapidMiner is a great tool for visual learners and rapid prototyping
