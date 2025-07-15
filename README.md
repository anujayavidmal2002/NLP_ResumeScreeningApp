# 📄 Resume Category Prediction App

A Machine Learning-powered web app that predicts the category of a resume (e.g., Data Science, Network Security Engineer, Advocate, etc.) using NLP and a Support Vector Machine classifier. Built using Python, scikit-learn, and Streamlit.

---

## 🚀 Features

- ✅ Upload resume files in `.pdf`, `.docx`, or `.txt` formats  
- 🔍 Clean and process resume content using NLP  
- ✨ Predict job category using a trained ML model (SVM with TF-IDF)  
- 📊 Supports over 25 resume categories  
- 🌐 Simple, interactive interface using Streamlit  

---

## 📂 Supported Resume Categories

Examples include:
- Data Science
- Network Security Engineer
- Advocate
- Health and Fitness
- Web Designing
- Java Developer
- Python Developer
- Sales
- DevOps Engineer
- HR
- Civil Engineer
- Mechanical Engineer
- Blockchain Developer  
... and many more

---

## 🧠 Model Architecture

- **Model**: Support Vector Classifier (SVC) using One-vs-Rest strategy  
- **Vectorization**: TF-IDF (Term Frequency-Inverse Document Frequency)  
- **Preprocessing**:
  - Remove URLs, mentions, hashtags
  - Remove special characters and punctuations
  - Lowercasing, whitespace removal

---

## 🛠️ Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/anujayavidmal2002/NLP_ResumeScreeningApp.git
cd NLP_ResumeScreeningApp
```

### 2️⃣ Install the required libraries
```bash
pip install -r requirements.txt
```

Or install them manually:
```bash
pip install streamlit scikit-learn pandas numpy matplotlib seaborn python-docx PyPDF2
```

### 3️⃣ Run the app
```bash
streamlit run app.py
```

---

## 📁 File Structure

```
.
├── app.py                    # Main Streamlit app
├── clf.pkl                   # Trained classifier (SVC)
├── tfidf.pkl                 # TF-IDF vectorizer
├── encoder.pkl               # LabelEncoder for category decoding
├── UpdatedResumeDataSet.csv # Original dataset (optional)
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation
```

---



## 📊 Model Training Summary

```python
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.svm import SVC
from sklearn.multiclass import OneVsRestClassifier
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
```

- Dataset: `UpdatedResumeDataSet.csv`
- Cleaned resumes
- Encoded with `LabelEncoder`
- Vectorized using `TfidfVectorizer`
- Model trained using `OneVsRestClassifier(SVC())`
- Accuracy: ~90% (on balanced data)

---

## 🧪 How to Test

You can test the app by uploading a resume in `.pdf`, `.txt`, or `.docx` format.  
Example categories include:
- 🧠 Data Scientist
- 🧑‍⚕️ Health and Fitness
- 🔐 Network Security Engineer
- ⚖️ Advocate

---

## 🧾 Example Resume Snippets

```
"Experienced Python Developer with background in machine learning, TensorFlow..."
→ Predicted Category: Python Developer

"Certified advocate with 10 years in civil and family law..."
→ Predicted Category: Advocate
```

---

## 🧰 Dependencies

- Python 3.7+
- Streamlit
- scikit-learn
- pandas, numpy
- matplotlib, seaborn
- PyPDF2
- python-docx

---

## ⚠️ Version Compatibility Warning

Scikit-learn model was saved using version **1.7.0**.  
To avoid version conflicts or `InconsistentVersionWarning`, make sure to use the same version or retrain the model in your own environment.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Anujaya Vidmal**  
🖥️ GitHub: [@anujayavidmal2002](https://github.com/anujayavidmal2002)  
📧 Email: anujayavidmal2002@gmail.com  
🏫 University of Moratuwa

---

## 📽️ YouTube Demo

🎥 Watch the full demo and tutorial:  
🔗 https://youtu.be/F3F6c0N12ls

---

## ⭐ Acknowledgments

- Dataset by Kaggle community  
- Streamlit team for the amazing web app framework
