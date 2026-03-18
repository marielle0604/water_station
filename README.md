**AquaVoice - Water Station Feedback System**
https://image.png

- A feedback management system for water refilling stations, developed as part of a Grade 12 ABM student research project. The system allows customers to submit feedback for different water stations and enables administrators to monitor and manage feedback effectively.

**Project Overview**
AquaVoice is a web-based application that bridges the gap between water refilling stations and their customers. It provides a platform for customers to share their experiences and for station administrators to monitor service quality and customer satisfaction.

**Key Features**
- Client Side
* Submit feedback for specific water stations
* Rate stations with star ratings (1-5)
* Provide detailed feedback and suggestions
* Optional contact information submission

- Admin Side
* Secure admin authentication
* Dashboard with key metrics:
* Total feedbacks received
* Average rating across all stations
* Number of active stations
* Station performance monitoring
* Recent feedbacks tracking
* User management interface

**Technology Stack**
- Backend: Python Flask
- Frontend: HTML, CSS, JavaScript
- Database: PostgreSQL
- Deployment: Railway.app

**Installation & Setup**
- Prerequisites
* Python 3.8 or higher
* PostgreSQL
* pip (Python package manager)

**Local Development Setup**
- Clone the repository
  * git clone https://github.com/marielle0604/water_station.git
cd water_station
- Create and activate virtual environment
  * python -m venv venv
      # On Windows
      venv\Scripts\activate
      # On Mac/Linux
      source venv/bin/activate
- Install dependencies
  * pip install -r requirements.txt
- Set up PostgreSQL database
  * CREATE DATABASE aquavoice;
    -- Run the schema.sql file to create tables
- Configure environment variables
   * DATABASE_URL=postgresql://username:password@localhost/aquavoice
   * SECRET_KEY=your_secret_key_here
- Run the application
  * python app.py
- Access the application
  * Customer portal: http://localhost:5000
  * Admin login: http://localhost:5000/admin/login

**Usage Guide**
- For Customers
 * Navigate to the feedback form
 * Select your water station from the dropdown
 * Enter your name and contact information (optional)
 * Provide your rating and feedback
 * Submit the form

- For Administrators
 * Login at /admin/login
 * Demo credentials: admin / admin123
 * View dashboard with key metrics
 * Monitor station performance
 * View recent feedbacksManage user accounts

**Database Schema**
-- Users table
CREATE TABLE users (
    id SERIAL PRIMARY KEY,
    username VARCHAR(50) UNIQUE NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    password_hash VARCHAR(200) NOT NULL,
    role VARCHAR(20) DEFAULT 'admin',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Stations table
CREATE TABLE stations (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    is_active BOOLEAN DEFAULT true,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Feedbacks table
CREATE TABLE feedbacks (
    id SERIAL PRIMARY KEY,
    station_id INTEGER REFERENCES stations(id),
    customer_name VARCHAR(100) NOT NULL,
    email VARCHAR(100),
    phone VARCHAR(20),
    rating INTEGER CHECK (rating >= 1 AND rating <= 5),
    feedback TEXT,
    suggestion TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

**Deployment**
The application is deployed on Railway.app:
* Live URL:(https://water-station-website-production-9018.up.railway.app/).
