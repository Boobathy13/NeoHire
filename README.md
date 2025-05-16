# 🤖 NeoHire – Smart Resume Shortlisting and Ranking System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Flask](https://img.shields.io/badge/Flask-API-lightgrey)
![spaCy](https://img.shields.io/badge/spaCy-en_core_web_trf-green)
![SBERT](https://img.shields.io/badge/SBERT-all--MiniLM--L6--v2-orange)
![MongoDB](https://img.shields.io/badge/MongoDB-NoSQL-brightgreen)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📌 Overview

**NeoHire** is an AI-powered resume shortlisting and Ranking system that uses **Natural Language Processing (NLP)** and **Semantic Similarity Models** to automate and enhance the hiring process. It parses resumes, extracts key details, and ranks them based on how well they match a job description — making the recruitment process faster, fairer, and smarter.

---

## ✨ Features

✅ Parse resumes in **PDF**, **DOCX**, or **scanned image** format
✅ Extract structured fields: **Name, Email, Skills, Experience, Education, Projects**
✅ Rank candidates using **semantic similarity (SBERT)** + **rule-based scoring**
✅ Visualize results with **score breakdowns** and **filters**
✅ Store and manage data in **MongoDB**
✅ Responsive **web interface** with **filter/search**

---

## 🧰 Tech Stack

| Layer          | Technology                                               |
| -------------- | -------------------------------------------------------- |
| **Frontend**   | HTML, CSS, JavaScript, Bootstrap                         |
| **Backend**    | Python 3.10, Flask                                       |
| **NLP Models** | spaCy `en_core_web_trf`, SBERT `all-MiniLM-L6-v2`        |
| **Libraries**  | PyMuPDF, python-docx, pytesseract, sentence-transformers |
| **Database**   | MongoDB (NoSQL)                                          |
| **Deployment** | Localhost (can be Dockerized or deployed to cloud)       |

---

## 🔧 Prerequisites

✅ Python 3.10+
✅ MongoDB
✅ pip and virtualenv
✅ Internet access to download NLP models

---

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/NeoHire.git
cd NeoHire
```

### 2️⃣ Set up a Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Download spaCy Transformer Model

```bash
python -m spacy download en_core_web_trf
```

---

## 🚀 Running the App

```bash
python app.py
```

App will start at:
🔗 [http://localhost:5000](http://localhost:5000)

---

## 🌐 API Endpoints

### 📤 Upload Resume

`POST /upload-resume`
Accepts: PDF, DOCX, PNG, JPEG

---

### 📝 Add Job Description

`POST /add-job`
**Payload:**

```json
{
  "title": "Data Analyst",
  "description": "Looking for experience in SQL, Python, Tableau"
}
```

---

### 📊 Rank Resumes

`GET /rank-resumes/<job_id>`
Returns: Ranked resumes with scores and matched fields

---

## 🧭 Project Structure

```
NeoHire/
├── app.py                        # Flask app entry point
├── DATABASE/                     # MongoDB operations
├── KEYWORDS/                     # Static keyword files (skills, tools)
├── MODELS/                       # spaCy and SBERT logic
│   ├── ner_parser.py             # spaCy NER model logic
│   └── sbert_ranker.py           # SBERT similarity logic
├── SCRIPTS/                      # Additional scripts/utilities
├── WEB_PAGE/                     # Frontend: HTML, CSS, JS
├── config.json                   # Configuration for job roles
├── db.env                        # MongoDB connection settings
├── ranking_cache.pkl            # Pickle cache for resume scores
├── resume_processing.log        # Log file for resume processing
├── app.log                      # General app logs
├── requirements.txt             # Python dependencies
└── README.md                    # You're reading it!
```

---

## 🚀 Future Enhancements

🌐 **Cloud Deployment:** Host on AWS, Azure, or GCP
🔍 **Advanced Filtering:** Filter resumes by skills, experience, or location
🧠 **Multilingual Support:** Extend spaCy to parse non-English resumes
💾 **Database Logging:** Track uploads, scores, and ranking history
🧾 **Export Results:** Export shortlisted resumes as PDF/CSV reports

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Authors

**KEVIN R, KIRAN AK, PREMASAGAR K, BOOBATHY R**

---
