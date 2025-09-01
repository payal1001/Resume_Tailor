# 🎯 AI-Powered Resume Tailor

An end-to-end web app that tailors your resume and generates a personalized cover letter for any job description using **GenAI**.  
Built with **FastAPI + Python** for backend, **React** for frontend, and **OpenAI / LLM APIs** for AI processing.  
Export polished **PDF highlighting key changes to the resume & generates a cover letter** with a single click.  

---

## ✨ Features
- 📤 Upload your resume (PDF)  
- 📝 Paste a job description  
- 🤖 AI tailors your resume & generates a cover letter  
- 💾 History stored in database (SQLite for dev, can upgrade to Postgres/MySQL)  
- 🔒 User authentication (email + password)  
- 📄 Export tailored resume + cover letter to PDF  
- 🎨 Modern, minimalist React frontend with animations  

---

## 🛠️ Tech Stack
**Backend**
- [FastAPI](https://fastapi.tiangolo.com/) (Python)
- [SQLAlchemy](https://www.sqlalchemy.org/) ORM
- [SQLite](https://www.sqlite.org/) (default DB)
- [JWT Authentication](https://jwt.io/)
- [ReportLab](https://www.reportlab.com/) (PDF generation)
- [OpenAI / OpenRouter](https://openrouter.ai/) API

**Frontend**
- [React](https://react.dev/)
- [CSS Modules](https://github.com/css-modules/css-modules) (styling)
- [React Icons](https://react-icons.github.io/react-icons/) (UI icons)

---

## 📂 Project Structure

```

resume-tailor/
│
├── resume-tailor-backend/   # FastAPI backend
│   ├── app/
│   │   ├── main.py
│   │   ├── models.py
│   │   ├── database.py
│   │   ├── auth.py
│   │   ├── routers/
│   │   │   ├── auth.py
│   │   │   ├── resume.py
│   │   └── utils/
│   │       ├── ai.py
│   │       ├── pdf.py
│   │
│   ├── requirements.txt
│
├── resume-tailor-frontend/  # React frontend
│   ├── src/
│   │   ├── pages/
│   │   │   ├── Register.js
│   │   │   ├── Login.js
│   │   │   ├── Dashboard.js
│   │   ├── services/
│   │       └── auth.js
│   │       └── resume.js
│   ├── App.js
│   ├── index.js
│   │── index.css
│   ├── package.json
│
└── README.md

````

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/resume-tailor.git
cd resume-tailor
````

---

### 2️⃣ Backend Setup (FastAPI)

```bash
cd resume-tailor-backend

# Create virtual environment
python -m venv venv
venv\Scripts\activate     # (Windows)
# OR
source venv/bin/activate  # (Linux/Mac)

# Install dependencies
pip install -r requirements.txt

# Run server
uvicorn app.main:app --reload
```

Backend will be live at 👉 `http://127.0.0.1:8000`

---

### 3️⃣ Frontend Setup (React)

```bash
cd ../resume-tailor-frontend

# Install dependencies
npm install

# Run development server
npm start
```

Frontend will be live at 👉 `http://localhost:3000`

---

## 🔑 Environment Variables

### Backend (`.env` in `resume-tailor-backend/`)

```env
OPENAI_API_KEY=your_openai_or_openrouter_key
JWT_SECRET=your_secret_key
JWT_ALGORITHM=HS256
```

### Frontend (`.env` in `resume-tailor-frontend/`)

```env
REACT_APP_API_URL=http://127.0.0.1:8000
```

---

## 📄 API Endpoints

| Method | Endpoint              | Description                  |
| ------ | --------------------- | ---------------------------- |
| POST   | `/auth/register`      | Register new user            |
| POST   | `/auth/login`         | Login & get JWT token        |
| POST   | `/resume/process`     | Upload resume + job desc     |
| POST   | `/resume/export/{id}` | Export tailored resume (PDF) |

---

## 🎨 UI Preview

* **Register / Login** → Modern gradient form with animations
* **Dashboard** → Upload resume + job description, get AI-tailored result
* **History** → View & export past tailored resumes

---

## 🛡️ Security Notes

* Passwords hashed with bcrypt
* JWT-based authentication
* DB is SQLite (dev) → swap to Postgres for production

---

## 📌 Roadmap

* [ ] Add job recommendation system
* [ ] Support multiple resume formats (.docx)
* [ ] Cloud storage (S3/GCP/Azure) for resumes
* [ ] Share resume via link

---

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📜 License

This project is licensed under the MIT License.
Feel free to use, modify, and share.

---

## 💡 Inspiration

Built to help job seekers quickly **stand out** by tailoring their resumes & cover letters with AI 🚀

