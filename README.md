# 🚀 Path Finder – Backend  
### AI-Powered Career Guidance Platform (Server Application)

---

## 📌 Project Overview

Path Finder Backend is the server-side application that powers the AI-driven career guidance platform.

It is built using **Node.js, Express, and PostgreSQL**, and provides RESTful APIs to handle:

- User authentication
- Career recommendation logic
- Session booking
- Goal tracking
- Forum management
- Job listings
- Database operations
- AI integration with OpenAI API

The backend serves both API endpoints and, in production, static frontend assets.

---

## 🛠 Tech Stack

### 🔹 Core Backend Technologies
- Node.js
- Express.js
- TypeScript

### 🔹 Database
- PostgreSQL
- Drizzle ORM

### 🔹 Authentication
- Express Session
- Passport.js (Local Strategy)

### 🔹 AI Integration
- OpenAI API

### 🔹 Deployment
- Render (Full-stack deployment)

---

## 🔗 API Documentation

Base URL (Production):

```
https://career-compass-updated-sax3.onrender.com/api
```

---

### 🔐 Authentication APIs

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/login` | User login |
| POST | `/api/register` | User registration |
| POST | `/api/logout` | Logout user |

---

### 👤 Profile APIs

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/profile` | Get user profile |
| PUT | `/api/profile` | Update profile |

---

### 🎯 Goals APIs

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/goals` | Get user goals |
| POST | `/api/goals` | Create new goal |
| PUT | `/api/goals/:id` | Update goal |
| DELETE | `/api/goals/:id` | Delete goal |

---

### 🧑‍💼 Sessions APIs

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/sessions` | Get sessions |
| POST | `/api/sessions` | Book session |

---

### 💼 Jobs APIs

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/jobs` | Get job listings |

---

### 💬 Forum APIs

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/forum` | Get forum posts |
| POST | `/api/forum` | Create post |
| POST | `/api/forum/:id/reply` | Add reply |

---

### 🤖 AI Recommendation API

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/ai/recommend` | Generate career recommendation |

This endpoint connects to the OpenAI API and generates structured career guidance based on user input.

---

## 🗄 Database Schema Explanation

The backend uses **PostgreSQL** with **Drizzle ORM** for schema management.

### Core Tables:

### 👤 Users
- id (Primary Key)
- email
- password (hashed)
- role

---

### 📄 Profiles
- id
- user_id (Foreign Key → Users)
- education
- skills
- interests
- experience

---

### 📅 Sessions
- id
- user_id (Foreign Key)
- counselor_id
- session_date
- status

---

### 🎯 Goals
- id
- user_id (Foreign Key)
- title
- description
- progress
- status

---

### 💼 Jobs
- id
- title
- description
- company
- location

---

### 💬 ForumPosts
- id
- user_id (Foreign Key)
- content
- created_at

---

### 💬 ForumReplies
- id
- post_id (Foreign Key)
- user_id (Foreign Key)
- content

---

### 🔗 Relationships

- One User → One Profile  
- One User → Many Goals  
- One User → Many Sessions  
- One Post → Many Replies  

---

## ⚙️ Installation Steps (Local Setup)

### 1️⃣ Clone Repository

```bash
git clone https://github.com/yasaswinireddy119/Backend-PathFinder.git
cd Backend-PathFinder
```

---

### 2️⃣ Install Dependencies

```bash
npm install
```

---

### 3️⃣ Configure Environment Variables

Create a `.env` file in root:

```
DATABASE_URL=your_postgresql_connection_string
AI_INTEGRATIONS_OPENAI_API_KEY=your_openai_api_key
```

⚠️ Never commit `.env` file to GitHub.

---

### 4️⃣ Push Database Schema

```bash
npm run db:push
```

---

### 5️⃣ Run Development Server

```bash
npm run dev
```

Backend runs at:

```
http://localhost:5001
```

---

### 6️⃣ Build for Production

```bash
npm run build
npm start
```

---

## 🌐 Deployment Link

🔗 **Live Backend (Full Stack Service):**  
https://career-compass-updated-sax3.onrender.com/

> The backend is deployed together with the frontend on Render.

---

## 🧠 Backend Architecture Overview

- Modular route structure
- Service-layer abstraction
- ORM-based database handling
- RESTful API design
- Environment-based configuration
- AI integration service layer
- Production-ready static serving

---

## 👩‍💻 Developed By

**Yasaswini Reddy**  
Full Stack Developer  
AI Enthusiast  

---
