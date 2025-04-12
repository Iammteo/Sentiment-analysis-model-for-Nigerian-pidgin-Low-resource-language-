
## 📝 Sentiment Analysis on Pidgin-English Reviews

This project performs **Sentiment Analysis** on Pidgin-English customer reviews using machine learning. It processes raw text reviews, extracts features using TF-IDF, and trains an SVM classifier to classify sentiments.

### 🚀 Features

- Supports **Pidgin-English** reviews (low-resource language)
- End-to-end ML pipeline with:
  - Text cleaning
  - TF-IDF vectorization
  - SVM classification
  - Hyperparameter tuning
- Evaluation metrics: Accuracy & Classification Report
- Runs smoothly in **Google Colab**


### 📁 Dataset

You can download the dataset directly using this link:

🔗 [Pidgin Reviews Dataset (.xlsx)](https://docs.google.com/spreadsheets/d/10y3SfW76BexZFp7AhE8q4HrhoJF9Op6u/edit?usp=sharing&ouid=116844381552592386775&rtpof=true&sd=true)

---

### 🧰 Requirements

You can run this in **Google Colab** without any setup.  
For local use, install the dependencies:

```bash
pip install pandas scikit-learn tabulate openpyxl
```

---

### 🧪 How to Use

#### In Google Colab:

1. **Import libraries and load the dataset:**

```python
import pandas as pd
import re
from sklearn.model_selection import train_test_split, GridSearchCV, RandomizedSearchCV
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import SVC
from sklearn.metrics import accuracy_score, classification_report
from sklearn.preprocessing import LabelEncoder
from tabulate import tabulate
from scipy.stats import uniform

# Load dataset from URL
url = "https://docs.google.com/spreadsheets/d/10y3SfW76BexZFp7AhE8q4HrhoJF9Op6u/edit?usp=sharing&ouid=116844381552592386775&rtpof=true&sd=true"
df = pd.read_excel(url)
print("Dataset loaded successfully!")
```

2. **Preprocess, train, and evaluate** the model using SVM and `GridSearchCV` or `RandomizedSearchCV`.

### 📊 Output

The script will output:
- Confirmation of dataset load
- Accuracy score
- Classification report (precision, recall, F1)


