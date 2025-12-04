🚗 QuickRide — Modern Full-Stack Ride Hailing Platform
<div align="center"> <img src="/Frontend/public/logo-quickride-green.png" height="110px" /> <br/> <strong>A streamlined, real-time ride booking experience—built from scratch.</strong> </div>

QuickRide is a complete ride-hailing ecosystem inspired by platforms like Uber and Ola, but engineered as a fully open, developer-friendly project. It demonstrates a production-ready architecture with real-time communication, live geolocation, intelligent ride allocation, and a responsive UI built for both riders and captains.

This repository is perfect for those who want to explore MERN stack, Google Maps API, Sockets, JWT Authentication, and real-world system design patterns.

📌 Table of Contents

Overview

Tech Stack

Key Features

Screens & UI Showcase

Getting Started

Environment Variables

Project Structure

Contributing

License

🧭 Overview

QuickRide mirrors the working of a real ride-sharing service:

Users request rides in real time

Captains receive live ride invitations

Both track each other with continuous location updates

A smart fare engine calculates cost based on distance/time

A socket-powered chat connects users during ongoing trips

The goal is not just to replicate existing platforms but to offer a clean architecture that learners can understand, extend, and deploy.

⚙️ Tech Stack
<div align="center"> <img src="https://skillicons.dev/icons?i=react,nodejs,express,mongo,tailwind,js,html,css,vercel,postman,git,npm,gmail&perline=7"/> </div>
Layer	Technologies
Frontend	React, Tailwind CSS, Vite, Google Maps JS SDK
Backend	Node.js, Express.js, MongoDB, Socket.IO, NodeMailer
Auth	JWT, bcrypt
Real-Time	WebSockets (Socket.IO)
Deployment	Vercel (Frontend), Render (Backend)
Developer Tools	Nodemon, ESLint, Postman, Custom Logging
✨ Key Features
🔐 Robust Authentication System

Secure login & registration (User & Captain)

JWT-based authentication with encrypted tokens

Email-based verification flow

Forgot/Reset password system

Protected routes with session validation

👤 User Capabilities

Update personal details (name, email, phone)

Track ongoing and past rides

View live captain movement on maps

Real-time chat during an active ride

Dynamic pricing and estimated arrival/distance preview

🚖 Ride Booking Engine

Three ride options: Car, Bike, Auto

Live states: Pending → Accepted → Ongoing → Completed → Cancelled

Intelligent concurrency control (only one captain can accept)

Auto-expire ride requests (timeout)

Accurate fare predictions based on route metrics

🗺️ Advanced Mapping & Geolocation

Address auto-suggest (Places API)

Turn-by-turn route display (Directions API)

Geo-tracking for both rider and captain

Smooth animations for points and routes

⚡ Real-Time Communication

WebSocket-powered ride status updates

Bi-directional live messaging between rider & captain

Location sync every few seconds

Stored chat history with timestamps

🎛️ Captain Dashboard

Accept/decline ride requests instantly

View rider pickup destination & summary

Track user in real time

Update ride progress dynamically

🧰 System-Level Utilities

Integrated logging system (frontend + backend)

Local data reset tool (helps during development)

Modular service-based backend architecture

Reusable UI components & state stores

🖼️ Screens & UI Showcase

All images stored inside: /Frontend/public/screens/

🔑 Authentication

📂 Sidebar Navigation

👤 User Dashboard

🚗 Captain Panel

⚡ Getting Started
1️⃣ Clone Repository
git clone https://github.com/Satyam-Mishra-1/QuickRide.git
cd QuickRide

2️⃣ Install Dependencies
Frontend
cd Frontend
npm install

Backend
cd ../Backend
npm install

3️⃣ Start Development Servers
Run Frontend (Vite)
npm run dev

Run Backend (Express)
npm run dev

4️⃣ Access Application

Frontend → http://localhost:5173

Backend → http://localhost:3000

🌍 Environment Variables

Create .env files inside both folders.

Frontend/.env
VITE_SERVER_URL=http://localhost:3000
VITE_ENVIRONMENT=development
VITE_RIDE_TIMEOUT=90000

Backend/.env
PORT=3000
RELOAD_INTERVAL=10
SERVER_URL=http://localhost:3000
CLIENT_URL=http://localhost:5173

ENVIRONMENT=development

MONGODB_PROD_URL=<mongo-atlas-url>
MONGODB_DEV_URL=mongodb://127.0.0.1:27017/quickRide

JWT_SECRET=<your-secret-key>

GOOGLE_MAPS_API=<google-maps-api-key>

MAIL_USER=<your-gmail>
MAIL_PASS=<your-app-password>

🗂️ Project Structure
QuickRide/
 ├── Frontend/       → React + Vite application
 ├── Backend/        → Express.js server
 ├── .gitignore
 ├── README.md
 └── package.json

🤝 Contributing

Contributions are always welcome!

⭐ Star the project

Fork the repository

Create a new feature branch

Commit your updates

Open a Pull Request