# 🌾 AgriDamage AI

### AI-Powered Crop Damage Detection & Farmer–Bank–Marketplace Integration System

---

## 📌 Table of Contents

* Overview
* Problem Statement
* Solution
* Key Features
* System Architecture
* Tech Stack
* Deep Learning Model
* Workflow
* Project Structure
* Installation Guide
* API Documentation
* Database Design
* User Roles
* Screenshots
* Future Enhancements
* Contributing
* License

---

## 🚀 Overview

**AgriDamage AI** is a full-stack web application that leverages **Deep Learning** to automate crop damage detection and streamline communication between **farmers, banks, and middlemen**.

Farmers can upload crop images along with essential details. The system uses a trained deep learning model to classify whether the crop is **damaged or undamaged**. Based on the result, the system notifies banks for verification and enables middlemen to connect directly with farmers for business opportunities.

This project combines **Artificial Intelligence + Web Development** to solve real-world agricultural problems.

---

## ❗ Problem Statement

Farmers face multiple challenges in the traditional agricultural ecosystem:

* Delays in crop damage verification
* Manual inspection processes
* Lack of transparency in insurance claims
* Limited access to buyers/middlemen
* Financial losses due to slow processing

---

## 💡 Solution

AgriDamage AI provides an automated and efficient solution:

* Farmers upload crop images
* AI model analyzes and classifies crop condition
* Data is stored securely in a database
* Banks receive damage reports instantly
* Middlemen can directly contact farmers

---

## ✨ Key Features

### 🤖 AI-Based Crop Classification

* Deep Learning model predicts:

  * Damaged
  * Undamaged

### 👨‍🌾 Farmer Module

* Upload crop images
* Enter:

  * Crop type
  * Quantity
  * Expected price
  * Cultivation duration
* Track submission status

### 🏦 Bank Module

* Receive damage alerts
* Verify claims
* Approve or reject requests

### 🧑‍💼 Middleman Module

* View farmer listings
* Contact farmers directly
* Negotiate prices

### 📊 Data Management

* Secure storage with MongoDB
* Efficient retrieval and updates

---

## 🏗️ System Architecture

Farmer → Upload Image + Data → Backend (Express API) → Deep Learning Model → Prediction → MongoDB → Bank & Middleman Access

---

## 🧰 Tech Stack

### Frontend

* React.js
* Axios
* CSS / Tailwind CSS

### Backend

* Node.js
* Express.js

### Database

* MongoDB

### AI / ML

* TensorFlow / PyTorch
* CNN (Convolutional Neural Network)

---

## 🧠 Deep Learning Model

* Model Type: Convolutional Neural Network (CNN)
* Task: Binary Image Classification

### Classes:

* Damaged
* Undamaged

### Model Pipeline:

1. Image preprocessing
2. Feature extraction using CNN layers
3. Fully connected layers
4. Output prediction

---

## 🔄 Workflow

1. Farmer logs into the system
2. Uploads crop image and details
3. Backend sends image to the AI model
4. Model predicts damage status
5. Result stored in MongoDB
6. If damaged → Bank is notified
7. Middleman views listing
8. Middleman contacts farmer

---

## 📁 Project Structure

agri-damage-ai/
│
├── frontend/          # React Application
│   ├── src/
│   ├── components/
│   └── pages/
│
├── backend/           # Express Server
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   └── middleware/
│
├── model/             # Deep Learning Model
│   ├── trained_model.h5 / .pt
│   └── inference script
│
├── config/            # Configuration files
│
└── README.md

---

## ⚙️ Installation Guide

### Clone Repository

git clone https://github.com/your-username/agri-damage-ai.git
cd agri-damage-ai

---

### Backend Setup

cd backend
npm install
npm run dev

---

### Frontend Setup

cd frontend
npm install
npm start

---

### Environment Variables (.env)

MONGO_URI=your_mongodb_connection
PORT=5000
MODEL_PATH=your_model_path

---

## 🔗 API Documentation

### Upload Crop Data

POST /api/upload

Request:

{
"image": "file",
"cropType": "Wheat",
"quantity": "100kg",
"expectedAmount": "5000",
"cultivationTime": "3 months"
}

Response:

{
"status": "success",
"prediction": "Damaged",
"message": "Report submitted successfully"
}

---

### Get All Reports

GET /api/reports

---

## 🗄️ Database Design

### Users Collection

* name
* role (farmer / bank / middleman)
* contact

---

### Crop Reports Collection

* image
* prediction
* cropType
* quantity
* expectedAmount
* cultivationTime
* status

---

## 👥 User Roles

### Farmer

* Upload crop data
* View results

### Bank

* Verify damage claims
* Approve or reject

### Middleman

* View farmer listings
* Contact farmers

---

## 📸 Screenshots

(Add screenshots of UI here such as upload page, dashboard, and results page)

---

## 🚀 Future Enhancements

* Mobile app using React Native
* Geo-location tagging
* Damage percentage prediction (not just binary)
* Weather API integration
* Blockchain-based record system
* WhatsApp/SMS notifications
* Market price prediction system

---

## 🤝 Contributing

Contributions are welcome.

Steps:

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

---

## 📜 License

This project is licensed under the MIT License

---

## ⭐ Final Note

This project demonstrates the power of combining **Artificial Intelligence with Full-Stack Development** to solve real-world agricultural problems. It has strong potential for hackathons, research, and placement portfolios.
