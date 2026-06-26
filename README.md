# 🩺 OncoPredict

### AI-Powered Cancer Risk Prediction & Clinical Decision Support System

<p align="center">

![React](https://img.shields.io/badge/Frontend-React%2018-61DAFB?style=for-the-badge\&logo=react)
![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=for-the-badge\&logo=node.js)
![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=for-the-badge\&logo=mongodb)
![Python](https://img.shields.io/badge/AI%2FML-Python-3776AB?style=for-the-badge\&logo=python)
![Docker](https://img.shields.io/badge/Deployment-Docker-2496ED?style=for-the-badge\&logo=docker)
![License](https://img.shields.io/badge/License-MIT-success?style=for-the-badge)

</p>

<p align="center">
An intelligent healthcare platform that combines <b>Artificial Intelligence</b>, <b>Machine Learning</b>, and <b>Modern Web Technologies</b> to assist doctors and radiologists in early cancer risk assessment from medical reports and diagnostic images.
</p>

---

# 📖 Overview

**OncoPredict** is a full-stack healthcare application designed to streamline the process of cancer risk assessment by integrating machine learning into the clinical workflow.

The platform enables **radiologists** to upload diagnostic reports, automatically analyzes them using an AI pipeline, assists **doctors** with clinical decision-making through risk prediction and structured summaries, and allows **patients** to securely access their reports through dedicated dashboards.

Instead of replacing medical professionals, OncoPredict is built as a **clinical decision support system**, helping healthcare providers prioritize high-risk cases, reduce manual workload, and improve diagnostic efficiency.

The project combines a **React frontend**, **Node.js backend**, **MongoDB database**, and a **Python-based machine learning pipeline** into a unified, modular, and scalable architecture.

---

# 🎯 Motivation

Early diagnosis significantly improves the chances of successful cancer treatment. However, hospitals often process a large number of diagnostic reports every day, making manual prioritization difficult.

OncoPredict was developed to assist healthcare professionals by:

* Automating medical report analysis
* Prioritizing patients based on predicted risk
* Reducing repetitive manual work
* Supporting doctors with AI-assisted insights
* Improving collaboration between radiologists, doctors, and patients
* Providing a centralized platform for report management

The objective is to make the diagnostic workflow faster, more organized, and easier to manage while ensuring that **final medical decisions always remain with healthcare professionals**.

---

# ✨ Key Features

## 🤖 AI-Assisted Risk Prediction

* Automated cancer risk prediction
* Machine learning-based classification
* Clinical feature extraction
* Explainable prediction pipeline
* Confidence score generation

---

## 🏥 Multi-Role Healthcare Platform

The application provides dedicated dashboards for different users.

### 👨‍⚕️ Radiologist

* Upload diagnostic reports
* Upload medical images
* View pending reports
* Track uploaded cases

### 🩺 Doctor

* Review AI predictions
* Validate reports
* Add clinical recommendations
* Monitor assigned patients

### 👤 Patient

* Access medical reports
* View prediction summaries
* Track diagnosis history
* Read simplified explanations

---

## 📄 Intelligent Report Processing

The system processes uploaded reports through multiple stages including:

* Medical text extraction
* Clinical preprocessing
* Feature generation
* AI inference
* Risk categorization
* Structured report generation

---

## 🔒 Secure User Management

* Role-based authentication
* Protected routes
* Separate dashboards
* Controlled access to medical information

---

## 📊 Dashboard Analytics

Users can monitor:

* Uploaded reports
* Pending reviews
* Prediction results
* Report history
* Patient records

---

# 🚀 Technology Stack

| Category   | Technologies                           |
| ---------- | -------------------------------------- |
| Frontend   | React 18, Vite, React Router, Axios    |
| Backend    | Node.js, Express.js                    |
| Database   | MongoDB, Mongoose                      |
| AI/ML      | Python, BioBERT, XGBoost, PyTorch, OCR |
| Deployment | Docker, Docker Compose, Nginx          |

---

# 🏗️ System Architecture

```text
                              Users
                                 │
        ┌────────────────────────┼────────────────────────┐
        │                        │                        │
        ▼                        ▼                        ▼
   Patient                  Doctor                 Radiologist
        │                        │                        │
        └────────────────────────┼────────────────────────┘
                                 │
                                 ▼
                      React Frontend (Vite)
                                 │
                      REST API (Express.js)
                                 │
          ┌──────────────────────┼──────────────────────┐
          │                      │                      │
          ▼                      ▼                      ▼
    MongoDB Database      AI Prediction Engine    File Storage
                                 │
                                 ▼
                     BioBERT + XGBoost Pipeline
```

The frontend communicates with the backend through REST APIs. The backend coordinates database operations, user authentication, file uploads, and communication with the machine learning pipeline. Prediction results are stored in MongoDB and delivered back to the appropriate dashboard.

---

# ⚙️ Core Modules

The application is organized into several independent modules.

| Module            | Responsibility                             |
| ----------------- | ------------------------------------------ |
| Authentication    | User login and role management             |
| Report Management | Uploading and organizing medical reports   |
| AI Prediction     | Cancer risk prediction using ML models     |
| Dashboard         | Personalized interfaces for each user role |
| Database          | Secure storage of reports and user data    |
| API Layer         | Communication between frontend and backend |

This modular design makes the application easier to maintain, extend, and deploy.

---

# 📋 Project Highlights

* Full-stack MERN architecture
* Integrated Python AI pipeline
* RESTful API design
* Role-based healthcare workflows
* Modular and scalable architecture
* Docker-based deployment support
* Separation of frontend, backend, and AI services
* Healthcare-oriented user experience

---

# 📌 Repository

**GitHub Repository:**
https://github.com/RDT556/OncoPredict

---
## 📂 Project Structure

The project follows a modular architecture that separates the frontend, backend, machine learning pipeline, and documentation. This organization improves maintainability, scalability, and collaboration.

```text
OncoPredict/
│
├── Code/
│   ├── frontend/          # React + Vite frontend
│   └── backend/           # Express.js backend + AI integration
│
├── Docs/                  # Project documentation & diagrams
│
├── docker-compose.yml
├── deploy.sh
├── backup.sh
├── stop.sh
├── check-requirements.sh
│
└── README.md
```

---

# 🖥️ Frontend Architecture

The frontend is built using **React 18** with **Vite** to provide a fast and responsive user experience.

### Responsibilities

* User Authentication
* Dashboard Rendering
* Report Upload
* Report Visualization
* API Communication
* Navigation
* Role-based Interface

The frontend communicates exclusively with the backend through REST APIs and never interacts directly with the database.

### Major Components

| Component             | Purpose                                    |
| --------------------- | ------------------------------------------ |
| Login                 | User authentication                        |
| Home                  | Landing page                               |
| Patient Dashboard     | Displays reports and prediction summaries  |
| Doctor Dashboard      | Reviews AI predictions and patient reports |
| Radiologist Dashboard | Uploads reports and manages worklist       |
| Reports               | Report management                          |
| Users                 | User management                            |

---

# ⚙️ Backend Architecture

The backend is developed using **Node.js** and **Express.js**, serving as the bridge between the frontend, database, and AI models.

### Responsibilities

* Authentication
* REST API
* Business Logic
* File Uploads
* Report Management
* Database Operations
* AI Pipeline Integration

Every request flows through the backend before reaching the database or machine learning pipeline.

```text
React Frontend
       │
       ▼
 REST API (Express)
       │
 ┌─────┴──────────┐
 │                │
 ▼                ▼
MongoDB      Python AI Engine
```

---

# 🤖 AI & Machine Learning Pipeline

One of the core features of OncoPredict is its AI-powered prediction engine.

The backend invokes Python scripts to analyze uploaded medical reports and generate risk predictions.

### Pipeline Workflow

```text
Medical Report
      │
      ▼
OCR Extraction
      │
      ▼
Clinical Text Processing
      │
      ▼
BioBERT Feature Extraction
      │
      ▼
Feature Engineering
      │
      ▼
XGBoost Prediction
      │
      ▼
Risk Classification
      │
      ▼
Prediction Summary
```

### Machine Learning Components

| Model          | Purpose                            |
| -------------- | ---------------------------------- |
| BioBERT        | Medical language understanding     |
| XGBoost        | Cancer risk classification         |
| OCR            | Extract text from uploaded reports |
| Feature Scaler | Normalize model inputs             |

The prediction results are stored in MongoDB and displayed on the respective dashboards.

---

# 🗄️ Database Design

The application uses **MongoDB** with **Mongoose** for flexible and scalable document storage.

### Primary Collections

### Users

Stores information about:

* Patients
* Doctors
* Radiologists

Typical fields include:

* Name
* Email
* Password
* Role
* Hospital
* Account Status

---

### Medical Reports

Each uploaded report contains:

* Patient Information
* Assigned Doctor
* Radiologist Details
* Uploaded File
* AI Prediction
* Risk Score
* Clinical Summary
* Review Status
* Upload Timestamp

---

# 🔄 System Workflow

The application follows a structured workflow that mirrors real-world hospital operations.

```text
Patient Registration
        │
        ▼
Radiologist Uploads Report
        │
        ▼
Backend Validation
        │
        ▼
AI Prediction Engine
        │
        ▼
Risk Assessment Generated
        │
        ▼
Doctor Reviews Report
        │
        ▼
Patient Views Final Report
```

This ensures that AI assists healthcare professionals while keeping the final diagnosis under the supervision of doctors.

---

# 🔐 Authentication & Authorization

OncoPredict follows a role-based access model.

| Role        | Permissions                                       |
| ----------- | ------------------------------------------------- |
| Patient     | View personal reports                             |
| Doctor      | Review AI predictions and manage assigned reports |
| Radiologist | Upload reports and monitor worklists              |

This separation ensures secure access to sensitive medical information.

---

# 📡 API Communication

The frontend communicates with the backend using RESTful APIs.

Typical operations include:

```http
POST   /login
POST   /upload
GET    /reports
GET    /reports/:id
PUT    /reports/:id
DELETE /reports/:id
```

Each request is validated before interacting with the database or AI pipeline.

---

# 📦 Docker-Based Deployment

The project is containerized using Docker for consistent deployment across different environments.

Services include:

* React Frontend
* Express Backend
* MongoDB Database

Deployment can be started using:

```bash
docker compose up --build
```

---

# 🧩 Design Principles

The project is designed around modern software engineering practices.

### ✔ Modular Architecture

Frontend, backend, AI models, and database are developed independently.

### ✔ Separation of Concerns

Each module has a clearly defined responsibility.

### ✔ Scalability

New AI models, dashboards, or APIs can be added without affecting existing components.

### ✔ Maintainability

Organized folder structure and reusable components simplify future development.

### ✔ Extensibility

The architecture supports future additions such as:

* JWT Authentication
* Cloud Storage
* Notification Services
* Admin Dashboard
* Additional ML Models

---

# 🎯 Technical Highlights

* MERN-based web application
* Python-powered AI prediction pipeline
* Role-based healthcare workflow
* RESTful API architecture
* Modular folder organization
* Docker containerization
* MongoDB document storage
* Scalable and maintainable design

---
# 🚀 Getting Started

Follow the steps below to set up and run the project locally.

## Prerequisites

Ensure the following software is installed on your system:

* Node.js (v18 or later)
* Python (v3.10+)
* MongoDB
* Docker & Docker Compose (Optional)
* Git

Verify your installation:

```bash
node -v
npm -v
python --version
docker --version
git --version
```

---

# 📥 Clone the Repository

```bash
git clone https://github.com/RDT556/OncoPredict.git

cd OncoPredict
```

---

# 📦 Backend Setup

Navigate to the backend directory:

```bash
cd Code/backend
```

Install Node.js dependencies:

```bash
npm install
```

Install Python dependencies:

```bash
pip install -r requirements.txt
```

Create a `.env` file and configure the required environment variables.

Start the backend server:

```bash
npm start
```

---

# 🌐 Frontend Setup

Navigate to the frontend directory:

```bash
cd Code/frontend
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

The frontend will be available at:

```
http://localhost:5173
```

---

# 🐳 Docker Deployment

The project also supports containerized deployment using Docker.

Build and start all services:

```bash
docker compose up --build
```

Stop all services:

```bash
docker compose down
```

---

# ⚙️ Environment Variables

Example backend configuration:

```env
PORT=5000

MONGODB_URI=your_mongodb_connection_string

NODE_ENV=development
```

Example frontend configuration:

```env
VITE_API_URL=http://localhost:5000/api
```

> Configure these variables according to your local or production environment.

---

# 🧪 Testing the Application

After starting all services:

* Log in using the appropriate user role.
* Upload a diagnostic report.
* Allow the AI pipeline to process the report.
* Review the generated prediction.
* Verify that the report is stored correctly in the database.

---

# 📈 Future Improvements

The current implementation establishes a strong foundation for AI-assisted clinical decision support. Future enhancements may include:

* JWT-based authentication
* Email notifications
* PDF report generation
* Cloud storage integration
* Real-time notifications
* Explainable AI visualizations
* Hospital analytics dashboard
* Appointment scheduling
* Multi-language support
* Model versioning
* Audit logging
* CI/CD pipeline integration

---

# 🤝 Contributing

Contributions are always welcome.

If you would like to contribute:

1. Fork the repository.
2. Create a new feature branch.

```bash
git checkout -b feature/your-feature
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push to your branch.

```bash
git push origin feature/your-feature
```

5. Open a Pull Request.

Please ensure that new features are properly documented and tested.

---

# 📚 Learning Outcomes

This project provided practical experience in:

* Full-Stack Web Development
* REST API Design
* React.js
* Express.js
* MongoDB
* Machine Learning Integration
* Medical Data Processing
* Docker Containerization
* Software Architecture
* AI-assisted Healthcare Systems

---

# 📌 Repository Structure Summary

| Layer      | Technology               |
| ---------- | ------------------------ |
| Frontend   | React, Vite              |
| Backend    | Node.js, Express         |
| Database   | MongoDB                  |
| AI/ML      | Python, BioBERT, XGBoost |
| Deployment | Docker                   |

---

# 💡 Why This Project?

OncoPredict demonstrates the integration of modern web technologies with machine learning to address a real-world healthcare problem.

The project showcases:

* End-to-end full-stack development
* AI model integration with a web application
* RESTful API development
* Modular architecture
* Role-based workflows
* Production-ready project organization

---

# 📄 License

This project is released under the **MIT License**.

You are free to use, modify, and distribute the project in accordance with the license terms.

---

# 👨‍💻 Author

**Anuj Tiwari**

* GitHub: https://github.com/RDT556

---

# ⭐ Support

If you found this project helpful, consider giving it a **⭐ Star** on GitHub.

It helps others discover the project and motivates future development.

---

<p align="center">

**Built with ❤️ using React, Node.js, MongoDB, Python, and Machine Learning**

</p>
