# NeuroLearn AI

NeuroLearn AI is a full-stack adaptive learning platform with:
- React frontend (Vite)
- FastAPI backend
- MongoDB persistence
- Groq-powered AI features

## Project Paths

- frontend app: frontend/
- backend app: backend/
- vercel config: vercel.json
- root ignore rules: .gitignore

## API Path Setup

All backend routes are mounted under /api:
- /api/health
- /api/auth/*
- /api/diagnostic/*
- /api/user/*
- /api/learning/*

Frontend API client uses:
- VITE_API_URL (defaults to /api)

This means frontend calls like /auth/login become:
- /api/auth/login

## Local Development

### Backend

From backend/:

1. Install dependencies
2. Run server

Example:

```powershell
c:/Users/Kaush/Desktop/ET-Hackathon/.venv/Scripts/python.exe -m pip install -r requirements.txt
c:/Users/Kaush/Desktop/ET-Hackathon/.venv/Scripts/python.exe -m uvicorn app.main:app --host 127.0.0.1 --port 8000
```

### Frontend

From frontend/:

1. Install dependencies
2. Start Vite dev server

Example:

```powershell
npm.cmd install
npm.cmd run dev
```

Vite proxy maps /api to http://127.0.0.1:8000 for local use.

## Environment Variables

### Backend (backend/.env)

Required for AI + DB:
- GROQ_API_KEY
- GROQ_MODEL
- GENAI_USE_LIVE
- MONGODB_URI
- MONGODB_DB

### Frontend (frontend/.env)

- VITE_API_URL=/api

## Vercel Deployment Path Setup

vercel.json rewrites API requests to the FastAPI serverless entrypoint:
- source: /api/(.*)
- destination: /backend/api/index.py

### Important Vercel Settings

Use one Vercel project with:
- Root Directory: repository root (ET-Hackathon)

If Root Directory is set to frontend/ only, /api routes will return NOT_FOUND because backend/ is outside that root.

## Secrets and GitHub Safety

- Keep real secrets in local backend/.env and Vercel env vars.
- Do not commit API keys.
- .gitignore excludes .env files and build/cache folders.

## Quick Verification Checklist

After deploy:

1. Open /api/health on your Vercel domain and confirm {"status":"ok"}
2. Test signup at /api/auth/signup via frontend Create Account flow
3. Confirm Vercel env vars are set for backend
