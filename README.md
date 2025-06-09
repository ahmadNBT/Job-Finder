# Job-Finder

# 🔥 Multi-Tenant Job Portal System

A full-featured multi-tenant job portal similar to Indeed, built with modern web technologies. This platform enables multiple companies to post jobs and interact with candidates through applications and real-time chat.

---

## 🚀 Features

### 🔐 Authentication
- Email/Password Login (JWT-based)
- Google Login (OAuth2 via Firebase or Passport.js)
- JWT Token Storage (localStorage or Cookies)

### 👥 User Roles
- **User (Candidate)**
- **Company (Employer)**

### 🏢 Company Features
- Company registration & profile creation
- Post jobs
- View applicants
- Chat with candidates
- Real-time notifications for new applications

### 👤 User Features
- Register/Login
- Apply to jobs
- View application history
- Chat with companies
- Get real-time job notifications

### 💬 Real-Time Chat
- User ↔ Company messaging
- Message history, read/unread status
- Built with **Socket.io**

### 🛎 Notification System
- Real-time notifications via Socket.io
- Stored in DB, visible on frontend

### 📄 Job Details Page
- View job info, required skills, company details
- Apply Now + Contact (chat)

### 📊 Dashboards
- User: Applications, saved jobs, notifications
- Company: Posted jobs, applicants

### 📁 Applications Management
- Jobs store applied users
- Users track applied jobs
- Company views full profiles

### 📅 Admin Panel (optional)
- Manage users, companies, job posts
- Block/delete suspicious accounts

---

## 🛠 Technology Stack

### Frontend
- Next.js
- Tailwind CSS
- Firebase (for Google Auth)
- Axios, Redux Toolkit (optional)
- Socket.io-client

### Backend
- Node.js + Express / NestJS (recommended)
- JWT, Bcrypt
- Firebase Admin SDK (Google token verification)
- Zod / Joi (validation)
- Socket.io

### Database
- PostgreSQL (with Prisma ORM) OR MongoDB (with Mongoose)

### Cloud & DevOps
- Vercel (Frontend)
- Railway / Render / Supabase (Backend & DB)
- Docker (optional)
- AWS EC2 (optional for backend)

### Optional Services
- SendGrid / Resend (emails)
- Redis (caching, online status)
- Cloudinary (media uploads)

---

## 🧭 Auth Flow Overview

1. **Custom Auth** → Email/password → JWT
2. **Google Auth (Frontend only)** → Firebase popup → Send ID token to backend → Verify & generate JWT
3. **Google Auth (Backend)** → Redirect to Google → Callback → JWT

---

## 🗄 Database Schema (PostgreSQL)

- **User**: id, name, email, password, role
- **Company**: id, name, logo, about, userId
- **Job**: id, title, description, companyId, createdAt
- **Application**: id, userId, jobId, resumeLink, status
- **Message**: id, fromUserId, toUserId, content, createdAt
- **Notification**: id, userId, type, readStatus, linkTo

---

## 📆 Development Timeline

| Week | Tasks |
|------|-------|
| **1** | Boilerplate, auth system, Google login, DB models |
| **2** | Job posting, job listing, apply system |
| **3** | Real-time chat, notification system |
| **4** | UI polish, dashboard, deployment, testing |

---

## 🧠 Future Enhancements

- Resume upload + parser
- Advanced filtering/sorting
- Saved jobs
- Analytics for companies
- Admin moderation panel

---

## 📄 License

MIT License © 2025
