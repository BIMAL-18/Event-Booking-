# Eventora -- (Bimal Kunwar) 🎟️
### Full-Stack Event Booking Platform

<p>
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB"/>
  <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express"/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js"/>
  <img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS"/>
  <img src="https://img.shields.io/badge/JWT-Auth-EF4444?style=for-the-badge&logo=jsonwebtokens&logoColor=white" alt="JWT"/>
</p>

<p>
  <img src="https://img.shields.io/badge/status-active-brightgreen?style=flat-square" alt="status"/>
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="license"/>
  <img src="https://img.shields.io/badge/PRs-welcome-orange?style=flat-square" alt="PRs welcome"/>
</p>

Eventora is a full-stack **MERN** application that allows users to seamlessly browse, register, and pay natively without any third-party tools. It features an administrative dashboard for event organizers to create and manage free and paid events, with all bookings manually verified and managed by an admin to handle payments directly.

---

## ✨ Features

- **User Authentication**
  Secure login & registration with JWT and bcrypt.

- **2FA OTP Verification**
  - Mandatory Email OTP to activate your account upon registration (or delayed login attempts).
  - Mandatory Email OTP to finalize and secure event ticket booking.

- **Role-Based Access**
  - **Admin:** Create, edit, and delete events. Confirm and reject all incoming booking requests, and mark them as `Paid` or `Not Paid`. Access is strictly locked to database-flagged users only.
  - **User:** Browse events, submit ticket booking requests via OTP, view a personal dashboard with pending status, and cancel bookings.

- **Event Management**
  Create free and paid events with detailed descriptions, external image URLs, dates, categories, and seating capacity.

- **Smart Booking System**
  - Mandatory 2FA OTP to authorize a booking request.
  - All booking requests (free and paid) enter a secure `Pending` queue for admin verification.
  - Seat availability accurately updates and securely validates against overbooking logic.

- **Admin Analytics Dashboard**
  Track live data such as Pending Requests, Total Revenue, and Total Confirmed Paid Clients directly from the admin panel.

- **Email Notifications**
  Automated email delivery upon successful booking confirmation using Nodemailer.

- **Sleek UI/UX**
  Built entirely with React and Tailwind CSS, polished with micro-interactions.

---

## 🛠️ Tech Stack

| Layer      | Technology                          |
|------------|--------------------------------------|
| 🎨 Frontend   | React, Tailwind CSS, Vite            |
| ⚙️ Backend    | Node.js, Express                     |
| 🗄️ Database   | MongoDB (Mongoose)                   |
| 🔐 Auth       | JWT, bcrypt, Email OTP (2FA)         |
| 📧 Email      | Nodemailer                           |

---

## 🚀 Setup Instructions

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed on your machine. You will also need a MongoDB database (e.g., [MongoDB Atlas Free Tier](https://www.mongodb.com/cloud/atlas/register)).

### 1. Environment Variables Configuration

Navigate to `server/.env` and fill in the necessary keys:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=supersecretjwtkey_eventora
EMAIL_USER=your_gmail_address
EMAIL_PASS=your_gmail_app_password
PORT=5000
```

> **Note:** For `EMAIL_PASS`, you need to generate an "App Password" from your Google Account settings — standard passwords won't work due to 2FA.

### 2. Run from Outer Folder (Single Terminal)

You can manage both backend and frontend from the project root:

```bash
# from Eventora root
npm install
npm run install:all
npm run dev
```

| Command            | Description                                                        |
|---------------------|---------------------------------------------------------------------|
| `npm run dev`       | Starts both `server` and `client` together using `concurrently`.   |
| `npm run dev:all`   | Installs dependencies (server + client) and starts both in one go. |
| `npm run start`     | Runs backend `start` + frontend `preview` together.                |

### 3. Install Dependencies (Manual / Two Terminals)

Alternatively, open two separate terminals for the backend and frontend.

**Backend Terminal:**
```bash
cd server
npm install --legacy-peer-deps
```

**Frontend Terminal:**
```bash
cd client
npm install
```

### 4. Run the Application Locally

**Run Backend:**
```bash
cd server
npm run dev
```
Server will run on `http://localhost:5000`

**Run Frontend:**
```bash
cd client
npm run dev
```
Client will run on a local port provided by Vite, typically `http://localhost:5173`

---

## 📄 License

This project is available for personal and educational use. Update this section with your preferred license (e.g., MIT) before publishing.
Ask Bimal Kunwar before using this Project 

---

<p align="center">Built by Bimal Kunwar using the MERN stack</p>

