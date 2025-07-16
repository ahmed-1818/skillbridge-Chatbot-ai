**Project: SkillBridge Chatbot Server**

The SkillBridge Chatbot Server is the backend API powering the SkillBridge AI platform — a smart assistant designed for students, freelancers, and project developers. It uses Flask for the backend, integrates with Groq/OpenAI for LLM responses, and optionally connects to Firebase and a vector database (FAISS/Pinecone) for advanced RAG-based conversations.

This server can:

Handle general chat queries from users

Process file-based queries (PDFs, CVs, etc.)

Log escalated queries for live human freelancers

Serve a built frontend (React) if deployed together

Connect with a freelancer dashboard for live support

**🚀 Features**
✅ RESTful Flask API

✅ LLM integration via Groq/OpenAI API

✅ File upload support for enhanced chat

✅ Human escalation with Firebase/JSON tracking

✅ RAG-ready structure (e.g., FAISS + prompt injection)

✅ Integrated frontend build serving (from /build)

✅ CORS support for smooth frontend-backend connection

✅ Railway/Render/Local deployment-ready

**📂 Folder Structure**

backend/
├── app.py                # Main Flask server
├── requirements.txt      # All Python dependencies
├── build/                # Compiled React frontend (optional)
├── firebase_config.json  # Firebase setup (if used)
├── uploads/              # Uploaded user files (ignored in Git)
├── utils/                # Helper functions
├── .env                  # API keys, kept secret
├── railway.json          # Deployment config for Railway



**📁 Sample API Endpoints**

| Method | Endpoint           | Description                   |
| ------ | ------------------ | ----------------------------- |
| POST   | `/api/ask`         | Main chat endpoint            |
| POST   | `/api/file-upload` | Uploads file for chat context |
| GET    | `/`                | Serves frontend index.html    |



**🧪 Technologies Used**

Python 3.10+
Flask
OpenAI / Groq API
Firebase Realtime DB
FAISS (for RAG)
React (Vite + ShadCN)
Tailwind CSS
Railway / Render


**🛠 Setup Instructions**

Clone the repo:
git clone https://github.com/ahmed-1818/backend.git
cd backend

Create a virtual environment:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

Install dependencies:
pip install -r requirements.txt

Add your .env file:
OPENAI_API_KEY=your_key
FIREBASE_KEY_PATH=firebase_config.json

Run the server:
python app.py
