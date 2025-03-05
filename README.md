# 🔒 File Sensitivity Classification using Metadata  

## 🚀 Project Overview  
In today's digital landscape, organizations deal with vast amounts of files, some of which contain **sensitive** information such as **personal identification documents, financial records, and confidential contracts**. Our project tackles the challenge of **automatically classifying files as Sensitive or Non-Sensitive** based solely on **metadata** like:  
✅ **File Name**  
✅ **File Path (Location)**  
✅ **File Extension**  

By leveraging **Machine Learning (ML) algorithms** and **Natural Language Processing (NLP) techniques**, we have developed a robust classification system that ensures data security and compliance.  

---

## 📊 Dataset Generation  
Since no readily available dataset suited our specific use case, we **created a custom dataset** containing **50+ metadata entries** representing real-world scenarios, ensuring diversity across:  
- **Personal and Government Documents** (Aadhar, PAN, Passport, etc.)  
- **Financial Records** (Bank Statements, Salary Slips, Tax Filings)  
- **Confidential Credentials** (Passwords, API Keys, Certificates)  
- **Regular Non-Sensitive Files** (Logs, Public Documents, Generic Text Files)  

Each record consists of:  
- **File Name**: The name of the file  
- **File Path**: The directory where the file is stored  
- **File Extension**: The file type  
- **File Size**: Optional metadata used for validation  

---

## 🧠 Approaches Used  

### 1️⃣ **Machine Learning-Based Classification**  
We employed **supervised learning** techniques to classify files into **Sensitive** or **Non-Sensitive** categories using:  
- **Random Forest Classifier** 🏆 (Best performer in terms of accuracy and robustness)  
- **Logistic Regression** (For interpretability and baseline comparisons)  

Each file's metadata was converted into **feature vectors**, and the models were trained using labeled data to recognize patterns indicating sensitivity.  

### 2️⃣ **NLP-Based Fuzzy Matching**  
To enhance accuracy, we implemented **NLP methods using the `fuzzywuzzy` module**, allowing the system to:  
✅ Detect partial matches between file names and known sensitive terms (e.g., “Aadhar_Scan” vs. “Adhar_copy”)  
✅ Handle variations in spellings and naming conventions  
✅ Improve recall by catching files that may evade strict rule-based filters  

---

## 🔬 Key Results & Performance  
Our combined **ML + NLP approach** significantly improved sensitivity classification:  
📈 **Random Forest achieved ~95% accuracy** on test data  
📉 **Logistic Regression performed well but was less robust to unseen data**  
📝 **Fuzzy Matching added flexibility**, boosting recall for mislabeled sensitive files  

---

## 🔧 How to Run the Project  
1️⃣ Install dependencies:  
```bash
pip install scikit-learn fuzzywuzzy pandas numpy
