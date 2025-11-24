# 🛡️ PhishDetector — Real-Time Phishing URL Detection System

PhishDetector is a full-stack phishing URL analysis system built using **React**, **Express.js**, and **PostgreSQL**, with real-time checks powered by **Google Safe Browsing API** and custom heuristic detection. Designed to identify malicious or suspicious URLs and provide a detailed risk evaluation.

---

## 🚀 Features

- 🔍 **Real-Time URL Scan** via Google Safe Browsing  
- 🧠 **Heuristic Pattern Matching** (URL structure, encoding, keyword flags)  
- ⚠️ **Risk Level Scoring** → Safe / Suspicious / Dangerous  
- 📜 **Scan History** stored per-user in PostgreSQL  
- 🔐 **Secure Signup & Login** using JWT authentication  
- 🧹 URL normalization & cleanup  
- ⚡ Fast & responsive UI with React + TailwindCSS  
- 🎥 Demo video included: `demo.mp4`

---

## 🛠️ Tech Stack

### **Frontend**
- React  
- Vite  
- Axios  
- TailwindCSS  

### **Backend**
- Node.js  
- Express.js  
- PostgreSQL  
- JWT Auth  
- Google Safe Browsing API  

---

## 📁 Folder Structure

```
phish-detector/
├── backend/
│   ├── controllers/
│   ├── routes/
│   ├── db/
│   ├── utils/
│   ├── app.js
│   └── server.js
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
└── phishdetectordemo.mp4
```

---

## 🔧 Requirements

Make sure you have installed:

- Node.js ≥ 18  
- PostgreSQL ≥ 13  
- npm or yarn  

---

## 🗄️ PostgreSQL Setup

Create a database and run the schema:

```
CREATE TABLE url_checks (
    id SERIAL PRIMARY KEY,
    user_email VARCHAR(255),
    url TEXT NOT NULL,
    risk_level VARCHAR(50),
    created_at TIMESTAMP DEFAULT NOW()
);
```

---

## 🔑 Environment Variables

Create a `.env` inside `/backend`:

```
PORT=5000
DATABASE_URL=postgresql://username:password@localhost:5432/your_db
JWT_SECRET=your_jwt_secret
GOOGLE_API_KEY=your_google_safebrowsing_key
```

---

## ▶️ Run the Project

### **Backend**
```
cd backend
npm install
npm start
```

### **Frontend**
```
cd frontend
npm install
npm run dev
```

---

## 🧪 API Endpoints

### POST `/api/check-url`
Analyzes and scores a URL.

### POST `/api/auth/signup`
Registers new user.

### POST `/api/auth/login`
Authenticates a user and returns JWT.

### GET `/api/history`
Fetches scan history for logged-in user.

---

## 📹 Demo
A working demo of the project is included as:

```
demo.mp4
```

---

