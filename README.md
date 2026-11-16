# 🧠 AI Resume Tailor API

An AI-powered FastAPI backend that **reads resumes**, **matches them to job descriptions**, and **suggests tailored improvements** to increase relevance for a specific role.

> ⚠️ This project provides **advisory insights only**. It does **not guarantee interviews or job offers**.

---

## 🚀 Features

* 📄 Upload resumes (PDF / DOCX)
* 🧩 Parse and extract resume content
* 🎯 Match resumes against job descriptions
* 🤖 AI-powered tailoring suggestions
* 📊 Resume–job relevance scoring (advisory)
* 🔌 Modular architecture (CRUD + AI separated)
* 🧪 API-first design (Swagger UI included)

---

## 🏗️ Architecture Overview

This project uses a **modular layered architecture** optimized for fast MVP development while remaining scalable for future growth.

```
Routes (FastAPI)
   ↓
Services (Business Logic)
   ↓
Utils / AI Modules
   ↓
Models (Schemas / DB)
```

✔ Not full Clean Architecture (yet)
✔ Not microservices (by design)
✔ AI logic is **decoupled** from CRUD

---

## 📁 Project Structure

```
resume_ai_app/
├─ main.py                 # FastAPI entry point
├─ routes/                 # API routes
│   ├─ resume.py
│   ├─ job.py
│   ├─ tailor.py
│   └─ ai_tailor.py
├─ services/               # Business logic
│   ├─ resume_service.py
│   ├─ job_service.py
│   └─ ai_service.py
├─ models/                 # Pydantic & DB models
│   ├─ schemas.py
│   └─ db_models.py
├─ utils/                  # Helpers
│   ├─ parser.py
│   ├─ nlp_utils.py
│   └─ file_utils.py
├─ ai_models/              # AI / ML logic (optional)
│   └─ job_match_model.py
├─ data/                   # Uploaded resumes & samples
├─ tests/                  # Unit & integration tests
└─ requirements.txt
```

---

## 🛠️ Tech Stack

* **Backend:** FastAPI
* **Language:** Python 3.10+
* **Parsing:** PDF / DOCX parsers
* **AI/NLP:** Embeddings / LLMs (pluggable)
* **Database:** SQLite (MVP)
* **Docs:** Swagger (OpenAPI)

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/ai-resume-tailor.git
cd ai-resume-tailor
```

### 2️⃣ Create virtual environment

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Run the server

```bash
uvicorn main:app --reload
```

---

## 📚 API Documentation

Once running, open:

* Swagger UI → [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
* ReDoc → [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## 🔌 Core Endpoints (MVP)

| Method | Endpoint         | Description           |
| ------ | ---------------- | --------------------- |
| POST   | `/resume/upload` | Upload a resume       |
| GET    | `/resume/list`   | List uploaded resumes |
| GET    | `/resume/{id}`   | Get parsed resume     |
| POST   | `/job`           | Add job description   |
| POST   | `/tailor`        | Rule-based tailoring  |
| POST   | `/ai-tailor`     | AI-powered tailoring  |
| POST   | `/predict`       | Advisory match score  |

---

## 🤖 AI Disclaimer (Important)

This project **does not predict hiring outcomes** with certainty.

* Scores are **heuristics or AI-assisted estimates**
* Results depend on data quality and job context
* Always use human judgment

---

## 🧪 Testing

```bash
pytest
```

---

## 🧭 Roadmap

* [ ] Improved resume parsing accuracy
* [ ] Better skill extraction
* [ ] Fine-tuned AI matching
* [ ] Frontend UI
* [ ] Docker support
* [ ] Optional Clean Architecture refactor
* [ ] Optional microservice split (AI engine)

---

## 🧠 Why This Project Exists

This project started as a **personal tool** to:

* Learn FastAPI + AI integration
* Automate resume tailoring
* Experiment with job–resume matching


---

## 📄 License

MIT. See [LICENSE](LICENSE).

---

## 🤝 Contributions

PRs, issues, and discussions are welcome but **keep it pragmatic**.
No over-engineering for the sake of architecture.
