# 📘 NeuroLearn – Behavior-Driven Adaptive Learning Platform

## 🚀 Overview

NeuroLearn is an AI-powered adaptive learning platform that detects **conceptual knowledge gaps using learner behavior** instead of relying solely on test scores.

It combines:
- **Behavioral analysis**
- **LLM-based evaluation**
- **Dynamic content generation**

to deliver **personalized learning experiences in real time**.

---

## 🎯 Problem Statement

Traditional learning systems:
- rely on quiz scores
- follow fixed learning paths
- fail to detect hidden misunderstandings

This leads to:
- false confidence
- inefficient learning
- lack of personalization

---

## 💡 Solution

NeuroLearn introduces a **behavior-driven learning intelligence layer** that:

1. Generates diagnostic questions for any topic  
2. Evaluates user responses using AI  
3. Detects:
   - weak concepts  
   - misconceptions  
   - confidence gaps  
4. Generates a **personalized learning plan**

---

## 🧠 Key Features

### ✅ Topic-Based Diagnostic System
- User enters any topic
- AI generates 3 high-quality diagnostic questions:
  - Conceptual
  - Application
  - Reasoning

---

### ✅ AI-Powered Evaluation
- Analyzes:
  - answer quality  
  - correctness  
  - confidence level  
- Detects:
  - misconceptions  
  - weak areas  
  - learning patterns  

---

### ✅ Personalized Learning Plan
- Generates:
  - simple explanations  
  - step-by-step learning path  
  - practice questions  
  - next steps  

---

### ✅ User Learning History
- Stores:
  - topics learned  
  - strengths & weaknesses  
  - progress level  
- Enables:
  - resume learning  
  - continuous personalization  

---

## 🏗️ System Architecture

Frontend (React + Vite)
        ↓
Backend (FastAPI)
        ↓
LLM Engine (Groq API)
        ↓
MongoDB (User Data + History)

---

## ⚙️ Tech Stack

### Frontend
- React.js (Vite)
- Tailwind CSS

### Backend
- FastAPI (Python)
- Mangum (for serverless deployment)

### AI / LLM
- Groq API (LLaMA models)

### Database
- MongoDB

### Deployment
- Vercel (Frontend + Serverless Backend)

---

## 📁 Project Structure

root/
├── frontend/        # React app
├── backend/         # FastAPI backend
│   └── api/
│       └── index.py # Vercel serverless entry
├── vercel.json
├── .gitignore

---

## 🔄 How It Works

1. User enters a topic  
2. AI generates diagnostic questions  
3. User submits answers + confidence  
4. AI evaluates responses  
5. System generates personalized learning plan  
6. Progress is stored for future sessions  

---

## 🧪 Example Flow

Input: "Recursion"

→ AI generates questions
→ User answers
→ System detects:
   - weak in base cases
→ AI responds with:
   - explanation
   - easier problem
   - next steps

---

## 🛠️ Setup Instructions

### 1. Clone Repository
git clone https://github.com/KNK2005/neurolearn.git
cd neurolearn

### 2. Frontend Setup
cd frontend
npm install
npm run dev

### 3. Backend Setup
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload

---

## 🔐 Environment Variables

Backend:
GROQ_API_KEY=your_api_key
GROQ_MODEL=your_model_name
GENAI_USE_LIVE=true
MONGODB_URI=your_mongodb_uri
MONGODB_DB=your_db_name

Frontend:
VITE_API_URL=/api

---

## 🚀 Deployment

Configured for deployment on Vercel.

---

## 🧭 One-Line Summary

NeuroLearn is an AI-powered adaptive learning system that detects knowledge gaps through behavior and delivers personalized learning experiences in real time.

---

## 👨‍💻 Author

Kaushik Nishaanth Kumar
