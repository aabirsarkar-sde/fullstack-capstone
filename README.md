# 📘 FeedbackFlow – A Student Feedback & Roadmap Portal

### 🚀 Project Proposal for Newton School

---

## 🧩 1. Overview

**FeedbackFlow** is a platform designed to improve transparency and collaboration between students and the Newton School administration.  
Currently, student feedback is private and individual, limiting visibility into what others are suggesting.  
FeedbackFlow aims to centralize student suggestions, enable upvoting on popular ideas, and display an official roadmap showing what’s planned, in progress, or launched.

---

## ⚠️ 2. Problem Statement

While Newton School’s platform offers various learning resources, the existing “Share a Concern” feature works as a one-to-one private channel.  
This approach:

- Prevents students from viewing or supporting feedback from peers.  
- Makes it harder for admins to identify high-impact suggestions.  
- Lacks transparency about which features are being addressed.  

**FeedbackFlow** solves this by creating a **public, community-driven feedback board** with voting and roadmap tracking.

---

## 🏗️ 3. System Architecture

**Architecture:**  
Frontend → Backend → Database  
`Next.js` → `Node.js REST API` → `MySQL (Prisma ORM)`

**Authentication:**  
JWT-based secure login system with two roles:
- **STUDENT:** Post feedback, comment, and upvote.  
- **ADMIN:** Manage posts and update their status.  

**Hosting:**  
- **Frontend:** Vercel  
- **Backend & Database:** Render 

---

## ✨ 4. Key Features

| Category | Features |
|-----------|-----------|
| **Authentication & Authorization** | Student registration, login, and logout. Role-based access for STUDENT and ADMIN. |
| **CRUD Operations** | Students can create feedback posts. Admins can update status or delete spam. |
| **Community Voting System** | Authenticated students can upvote feedback posts to highlight popular ideas. |
| **Advanced Filtering & Sorting** | Sort by *Most Upvoted* or *Most Recent*. Filter by category or status. |
| **Public Roadmap** | A visual page displaying items marked as *Planned*, *In Progress*, or *Launched*. |
| **Frontend Routing** | Pages include: Home, Login/Register, Feedback Board, Roadmap, and Admin Dashboard. |

---

## 🧠 5. Tech Stack

| Layer | Technologies |
|--------|---------------|
| **Frontend** | Next.js, React, Axios, TailwindCSS |
| **Backend** | Node.js, Express.js |
| **Database** | MySQL with Prisma ORM |
| **Authentication** | JSON Web Tokens (JWT) |
| **Hosting** | Vercel (Frontend), Render/Railway (Backend) |

---

## 🔌 6. API Overview

| Endpoint | Method | Description | Access |
|-----------|--------|--------------|--------|
| `/api/auth/signup` | POST | Register a new student | Public |
| `/api/auth/login` | POST | Authenticate user and return JWT | Public |
| `/api/feedback` | GET | Get all feedback posts (paginated) | Public |
| `/api/feedback` | POST | Create a new feedback post | Authenticated |
| `/api/feedback/:id/vote` | POST | Upvote a specific feedback post | Authenticated |
| `/api/feedback/:id/status` | PUT | Update feedback status (e.g., "Planned") | Admin |
| `/api/feedback/:id` | DELETE | Delete a feedback post | Admin |

---

## 🧭 7. Future Enhancements

- Add comments and discussion threads on feedback posts.  
- Introduce email or in-app notifications for updates.  
- Enable tag-based categorization for better discoverability.  

---

## 🧑‍💻 Contributors
- **Aabir Sarkar** – Project Lead & Developer  

---

> 🧱 *FeedbackFlow fosters an open feedback culture, allowing Newton School students to shape their learning experience together.*
