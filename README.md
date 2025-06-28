# 🐳 Dockerized MySQL: Airplane Passengers Database

This project demonstrates how to containerize a MySQL database using Docker. It automatically sets up a 'FlightEn' database and imports predefined passenger data from a '.sql' file during container startup.

---

## 📌 Project Overview

- Creates a custom MySQL image using 'mysql:8.0' as the base.
- Loads 'FlightEn.sql' to automatically create and populate the 'flight_bookings' table.
- Exposes MySQL on port '3307' for local access.
- Uses secure environment variables for root and user credentials.

---

## 🗂️ Folder Structure

DATABASE/
├── Dockerfile
└── FlightEn.sql

---

## ⚙️ Environment Configuration

- MYSQL_ROOT_PASSWORD
- MYSQL_DATABASE
- MYSQL_USER=admin`
- MYSQL_PASSWORD

---


### 🛠️ Build the Docker Image

'docker build -t flighten-mysql .'

### 🐳 Run the Container

'docker run --name flighten-db -p 3307:3306 -d flighten-mysql'

### 🔐 Connect to MySQL

'docker exec -it flighten-db mysql -u root -p'
# Enter password: 

### 🧾 Query the Data


USE FlightEn;
SELECT * FROM flight_bookings;

---

## 🧠 Learning Outcomes

- Dockerfile writing and MySQL containerization
- Automatic SQL data seeding using Docker volumes
- Working with MySQL in isolated environments
- Secure credential handling using environment variables

---

## 👨‍💻 Author

Abdulharis Shaikh 
DevOps Enthusiast & Cloud Learner  
📍 India | 💻 Python | ☁️ Docker | ⚙️ Engineering Student

---

Thank You
