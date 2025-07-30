# 🧠 AI Micro-Frontend Playground

A full-stack AI-powered web playground that lets users generate, preview, and edit micro-frontend components using natural language prompts.

> Built using **Next.js (App Router)**, **Express.js**, **MongoDB**, and **OpenRouter (GPT-like AI)**.

---

## ✨ Features

- ✅ User Authentication (Register / Login)
- 💬 Chat interface to prompt AI
- ⚛️ JSX + CSS generation from natural prompts
- 🔁 Live React preview using Babel in-browser
- 💾 Auto-saving of code and chat history
- 🌐 Fullstack architecture (separate frontend + backend)
- 🚀 Deployed on Vercel + Render

---

## 🏗️ Tech Stack

| Layer        | Tech             |
|--------------|------------------|
| Frontend     | Next.js 15 (App Router), Tailwind CSS |
| Backend      | Node.js, Express.js |
| AI Service   | OpenRouter (GPT-like API) |
| Database     | MongoDB + Mongoose |
| Auth         | JWT (httpOnly cookies) |
| Hosting      | Vercel (frontend), Render (backend) |

---

## 🧩 Folder Structure

```

frontend/
├── app/
│   ├── login/
│   ├── register/
│   └── playground/\[id]/
│       ├── ChatPanel.tsx
│       ├── PreviewFrame.tsx
│       └── CodeTabs.tsx
├── lib/
│   └── axios.ts (axios config)
└── ...
backend/
├── models/
├── controllers/
├── routes/
├── services/
└── server.js

````

---

## 🔐 Environment Variables

### Backend (`.env` on Render):

```env
PORT=5000
MONGO_URI=mongodb+srv://<user>:<pass>@cluster.mongodb.net/db
JWT_SECRET=your_jwt_secret
OPENROUTER_API_KEY=your_openrouter_api_key
````

### Frontend (`.env.local` for Vercel):

```env
NEXT_PUBLIC_API_BASE_URL=https://backend-cf-2213.onrender.com
```

---

## 🚀 Deployment

### ✅ Backend on Render

1. Push `backend` code to GitHub
2. Create new **Render Web Service**
3. Set `build` command: `npm install`
4. Set `start` command: `node server.js`
5. Add environment variables
6. Copy live backend URL

### ✅ Frontend on Vercel

1. Push `frontend` code to GitHub
2. Import repo into [vercel.com](https://vercel.com/)
3. Set `NEXT_PUBLIC_API_BASE_URL` in project settings
4. Deploy and enjoy 🎉

---


## 🧠 AI Prompt Format

You can prompt like:

```
Create a login form with email and password inputs, styled with Tailwind.
```

The AI returns:

* `JSX`: main component
* `CSS`: optional styling (or Tailwind classes)

---

## 🛠️ Local Development

### Backend

```bash
cd backend
npm install
npm run dev
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

---
