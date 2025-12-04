<div align="center">
    <!-- Main Logo -->
    <img src="/Frontend/public/logo-quickride-green.png" height="110px" alt="QuickRide Logo"/>
</div>

<h1 align="center">🚖 QuickRide – Full Stack Ride Booking Platform</h1>

<p align="center">
A modern, robust, and feature-rich full-stack ride-booking application inspired by top mobility platforms like Uber & Ola.  
QuickRide demonstrates real-time communication, location tracking, interactive UI, Google Maps integration, authentication, and a complete user–captain ecosystem — all wrapped in a clean and functional experience.
</p>

<div align="center">
    ⭐ If you like this project, please star the repository — your support motivates further development! ⭐  
</div>

---

## 📚 Table of Contents
1. [Tech Stack](#-tech-stack)
2. [Features](#-features)
3. [Screenshots](#-screenshots)
4. [Quick Start](#-quick-start)
5. [Environment Variables](#-environment-variables)
6. [Project Architecture](#-project-architecture)
7. [API Overview](#-api-overview)
8. [Contributing](#-contributing)
9. [License](#-license)

---

## ⚙️ Tech Stack

<div align="center">
  <img src="https://skillicons.dev/icons?i=html,css,js,react,nodejs,express,mongo,tailwind,gcp,vercel,git,postman,npm&perline=8"/>
</div>

| Category | Technologies |
|---------|--------------|
| **Frontend** | React.js, TailwindCSS, Google Maps SDK, Vite |
| **Backend** | Node.js, Express.js, MongoDB, Socket.IO |
| **Real-Time** | WebSockets (Socket.IO) |
| **Authentication** | JWT, bcrypt |
| **Email Services** | NodeMailer |
| **Deployment** | Vercel (Frontend), Render (Backend) |
| **Developer Tools** | Postman, Nodemon, ESLint, Custom Logger |

---

## ✨ Features

### 🔐 Authentication & Authorization
- Fully secure JWT-based login system  
- Email verification & session handling  
- Strong validation on all forms  
- Role-based access: **User / Captain**  

### 🧑‍💼 User Dashboard
- Profile management  
- Ride history  
- Live ride status tracking  

### 📍 Real-Time Location & Mapping
- Google Places auto-complete  
- Real-time captain & rider tracking  
- Route preview with distance & ETA  
- Accurate fare prediction  

### 🚖 Ride Booking System
- Ride types: **Car, Bike, Auto**  
- Live updates: Pending → Accepted → Ongoing → Completed  
- Captain concurrency control (only one can accept)  
- Automatic ride cancellation after timeout  

### 🔄 Real-Time Communication
- In-app live chat (User ↔ Captain)  
- Chat stored with timestamps  
- Only matched user/captain can access chat  

### 👨‍✈️ Captain Interface
- Accept / reject rides  
- Live location broadcasting  
- Trip status management  

### 🧰 System Utilities
- Persistent log storage (Frontend + Backend)  
- One-click force reset (clears all data)  
- Smart popup system for alerts (success/error/info)  

---

## 🖼️ Screenshots

> All screenshots are stored inside  
> **`/Frontend/public/screens/`**

### 🔑 Authentication
![User Auth](./Frontend/public/screens/user-auth.png)

### 📂 Sidebar Navigation
![Sidebar](./Frontend/public/screens/sidebar.png)

### 👤 User Module
![User Module](./Frontend/public/screens/user-module.png)

### 🚕 Captain Module
![Captain Module](./Frontend/public/screens/captain-module.png)

---

Here is a **super improved**, **hyper-clean**, **aesthetic**, **professional**, **developer-friendly**, and **GitHub-premium style** rewrite of your entire **Quick Start** + **Env Vars** + **Project Architecture** + **API Overview** section.

It is designed to look like a **top-tier open-source project**, similar to production-level READMEs.

You can **copy–paste directly** into your README.

---

# ⚡ **Quick Start**

Follow these steps to set up and run the QuickRide development environment smoothly.

---

## 📁 **Project Structure**

```bash
QuickRide
│── Backend/      # Node.js, Express, MongoDB, Socket.IO, Nodemailer
│── Frontend/     # React, Vite, Tailwind CSS, Google Maps SDK
```

---

# 🚀 **1️⃣ Clone the Repository**

```bash
git clone https://github.com/Satyam-Mishra-1/QuickRide.git
cd QuickRide
```

---

# 📦 **2️⃣ Install Dependencies**

### **Frontend Installation**

```bash
cd Frontend
npm install
```

### **Backend Installation**

```bash
cd ../Backend
npm install
```

---

# 🛠️ **3️⃣ Run Development Servers**

### **Start Frontend (React + Vite)**

```bash
npm run dev
```

### **Start Backend (Node.js + Express)**

```bash
npm run dev
```

---

# 🌍 **4️⃣ Access the Application**

| Service      | URL                                            |
| ------------ | ---------------------------------------------- |
| **Frontend** | [http://localhost:5173](http://localhost:5173) |
| **Backend**  | [http://localhost:3000](http://localhost:3000) |

---

# 🌐 **Environment Variables**

Create `.env` files in **Frontend** and **Backend** directories.

---

## 🎨 **Frontend `.env`**

```env
VITE_SERVER_URL=http://localhost:3000
VITE_ENVIRONMENT=development
VITE_RIDE_TIMEOUT=90000
```

---

## 🧪 **Backend `.env`**

```env
PORT=3000
RELOAD_INTERVAL=10

SERVER_URL=http://localhost:3000
CLIENT_URL=http://localhost:5173
ENVIRONMENT=development

MONGODB_PROD_URL=<your-mongodb-atlas-url>
MONGODB_DEV_URL=mongodb://127.0.0.1:27017/quickRide

JWT_SECRET=<your-jwt-secret>
GOOGLE_MAPS_API=<your-google-maps-api-key>

MAIL_USER=<your-gmail-id>
MAIL_PASS=<your-gmail-app-password>
```

---

# 🧩 **Project Architecture**

A clean and scalable architecture is followed for better maintainability.

---

## 🎨 **Frontend Structure**

```bash
Frontend/
│── components/        # Reusable UI components
│── context/           # Global state & auth providers
│── hooks/             # Custom React hooks
│── pages/             # Application pages (User/Captain)
│── utils/             # Utility functions
│── services/          # API calls (axios services)
```

---

## ⚙️ **Backend Structure**

```bash
Backend/
│── routes/            # API endpoints
│── controllers/       # Route controllers (business logic)
│── models/            # Mongoose models (User, Ride, Chat)
│── middleware/        # Auth, validation, error handling
│── services/          # Email service, fare calculation, helpers
│── utils/             # Loggers, config, validators
│── sockets/           # Real-time ride & chat via Socket.IO
```

---

# 📡 **API Overview**

**Base URL:** `http://localhost:3000/api`

| Module      | Endpoints                                        |
| ----------- | ------------------------------------------------ |
| **Auth**    | `/signup`, `/login`, `/verify-email`, `/logout`  |
| **User**    | `/profile`, `/update-profile`, `/ride-history`   |
| **Captain** | `/accept-ride`, `/update-status`                 |
| **Ride**    | `/create-ride`, `/calculate-fare`, `/track-ride` |
| **Chat**    | `/messages`, `/send`                             |

> 📌 *Full Postman API Collection is included in the repository.*

---

# 🤝 **Contributing**

We appreciate and welcome contributions!

1. **Fork** this repository
2. **Create** a new branch

   ```bash
   git checkout -b feature/new-feature
   ```
3. **Commit** your changes
4. **Push** to your branch
5. **Open a Pull Request** 🚀

---
