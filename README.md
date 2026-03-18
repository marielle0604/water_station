# Flask Project

A Flask web application.

# About
- A grade 12 ABM Research PrOject
#  Water Station Management System

A full-stack web application for managing a water refilling station.
Built using **React (Vite)** for the frontend and **Node.js + Express + PostgreSQL** for the backend.

---

##  Features
- Client Side

* User Registration & Login
* User Profile Management
* Book Appointments (Water Delivery / Pickup)
* Send Feedback
* View Transaction History
* Responsive Design (Mobile-Friendly)

---

- Admin Dashboard

* View Customer Feedback
* Manage Appointments
* Monitor Inventory (Water gallons, supplies)
* View Daily & Yearly Analytics
* Track Transactions

---

##  Tech Stack
- Frontend

* React (Vite)
* React Router
* CSS / Responsive Design

- Backend

* Node.js
* Express.js
* PostgreSQL
* JWT Authentication

---

##  Project Structure

```
water-station/
│
├── frontend/
│   └── src/
│       ├── components/
│       ├── pages/
│       └── App.jsx
│
├── backend/
│   ├── server.js
│   ├── db.js
│   ├── routes/
│   ├── controllers/
│   └── models/
│
└── README.md
```

---



### 1️ Clone the Repository

```
git clone https://github.com/your-username/water-station.git
cd water-station
```

---

### 2️Setup Backend

```
cd backend
npm install
```

Create `.env` file:

```
PORT=5000
DATABASE_URL=postgresql://postgres:yourpassword@localhost:5432/waterstation
JWT_SECRET=your_secret_key
```

Run backend:

```
npm run dev
```

---

### 3️Setup PostgreSQL
Login to PostgreSQL:

```
sudo -u postgres psql
```

Create database:

```
CREATE DATABASE waterstation;
```

---

### 4️Setup Frontend

```
cd ../frontend
npm install
npm run dev
```

Open in browser:

```
http://localhost:5173
```

---

## Authentication

* Uses JWT (JSON Web Token)
* Secure login & protected routes
* Role-based access (Admin & Client)

---

## Sample Modules

* **Appointments** – Schedule water delivery
* **Feedback** – Customer suggestions & issues
* **Inventory** – Track water gallons & supplies
* **Transactions** – Payment and order records
* **Analytics** – Daily & yearly reports

---

## Responsive Design

* Works on desktop, tablet, and mobile devices
* Optimized UI for better user experience

---

## Future Improvements

* Payment Integration (GCash / PayMaya)
* SMS/Email Notifications
* Real-time updates using WebSockets
* Map integration for delivery tracking

---

## Author

**Marielle Modesto**
BS Information Technology Student


#Deployed in Railway:
- https://water-station-website-production-9018.up.railway.app/
