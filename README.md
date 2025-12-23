# Hostel Hub – Hostel Management System with NLP & LLM Integration

A full-stack **Hostel Management System** built using **Flask**, integrating **classical NLP, machine learning, LLM-based intent analysis**, and deployed on **AWS EC2**.  
The project focuses on automating hostel operations such as **issue categorization**, **student exit management**, and **nearby marketplace discovery** using intelligent text understanding.

---

## 🚀 Features

### 🔹 Issue Management with NLP
- Users submit issues in **free-text form**
- Automatic **issue category prediction** using **TF-IDF + Linear SVM**
- Basic **sentiment and priority understanding**
- Enables faster and automated worker assignment

### 🔹 Hostel Exit Intent Analysis (LLM-based)
- Supports:
  - Regular hostel exits
  - Long leaves (vacation / extended stay outside hostel)
- Uses:
  - **Local Qwen-2.5 model** for intent understanding
  - Extracts:
    - Leave type
    - Expected duration
    - Return estimation
    - Risk indicators (late return, unusual patterns)
- Reduces manual approval overhead

### 🔹 Nearby Marketplace Search
- Marketplace search for items like:
  - Electronics
  - Sports equipment
  - Daily essentials
- Uses **OpenStreetMap (OSM) data**
- NLP-based keyword mapping for relevant shop discovery

### 🔹 Deployment
- Backend deployed on **AWS EC2**
- Headless and production-ready setup
- Designed for further scalability

---

## 🧠 NLP & Machine Learning Pipeline

### 1️⃣ Text Preprocessing
- Lowercasing
- Punctuation removal
- Stopword removal
- Lemmatization

### 2️⃣ Feature Extraction
- **TF-IDF Vectorization**
- Converts unstructured text into numerical features

### 3️⃣ Model Used
- **Linear Support Vector Machine (SVM)**
- Well-suited for high-dimensional sparse text data
- Chosen over Naive Bayes due to better class separation

### 4️⃣ Evaluation
- Train/Test split
- Accuracy-based evaluation
- Confusion matrix analysis for misclassification insights
- Achieved **~85–90% accuracy** on issue categorization

---

## 🏗️ Tech Stack

### Backend
- Flask (Python)
- Flask-JWT (Authentication)
- SQLAlchemy / PostgreSQL

### NLP & ML
- Scikit-learn
- TF-IDF Vectorizer
- Linear SVM
- NLTK (text preprocessing)

### LLM
- Local **Qwen-2.5** model
- Basic LLM API calls for intent understanding

### External APIs
- OpenStreetMap (Nearby shop search)

### Deployment
- AWS EC2
- Gunicorn
- Headless server configuration

---

## 📂 Project Architecture (High-Level)

