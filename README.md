# Curely - Healthcare Management System & AI Symptom Checker

**Curely** is a full-stack healthcare platform designed to bridge the gap between patients, doctors, and diagnostic labs. It features role-based dashboards, appointment management, medical report handling, and an AI-powered chatbot for preliminary symptom analysis and disease prediction.

## 🚀 Features

### 👤 Customer (Patient)

* **Dashboard:** Overview of health stats and upcoming activities.
* **Appointments:** Book and manage appointments with doctors.
* **Prescriptions:** View digital prescriptions issued by doctors.
* **Reports:** Access and download lab reports uploaded by diagnostic centers.
* **AI Symptom Checker:** Input symptoms to get preliminary disease predictions using a Machine Learning model.

### 👨‍⚕️ Doctor

* **Dashboard:** Manage patient queues and appointments.
* **Consultation:** Issue digital prescriptions.
* **Patient History:** View patient medical reports and history.

### 🔬 Lab (Diagnostic Center)

* **Dashboard:** View pending test requests.
* **Report Management:** Upload patient medical reports (PDF support).

### 🤖 AI Chatbot Service

* **Disease Prediction:** Uses a Python-based Machine Learning model to predict top 3 potential diseases based on user-rated symptoms.
* **Dynamic Questioning:** Generates follow-up questions to refine symptom description.

---

## 🛠️ Tech Stack

### **Frontend**

* **Framework:** React (Vite)
* **Styling:** Tailwind CSS, CSS Modules
* **Routing:** React Router DOM
* **Icons:** Lucide React
* **HTTP Client:** Axios

### **Backend (Main API)**

* **Runtime:** Node.js
* **Framework:** Express.js
* **Database:** MongoDB (Mongoose)
* **Authentication:** JWT (JSON Web Tokens) & Bcryptjs
* **File Handling:** Multer (for report uploads)
* **Email:** Nodemailer

### **AI Chatbot Service**

* **Language:** Python
* **Framework:** Flask
* **ML Libraries:** Scikit-learn, Pandas, NumPy, Joblib

---

## ⚙️ Installation & Setup

### Prerequisites

* Node.js (v14+)
* Python (v3.8+)
* MongoDB (Local or Atlas connection string)

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/curely-v1.git
cd curely-v1

```

### 2. Backend Setup (Node.js)

Navigate to the backend folder, install dependencies, and start the server.

```bash
cd backend
npm install

```

**Configuration:**
Create a `.env` file in the `backend` directory with the following variables:

```env
PORT=3001
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
# Optional (for email features)
EMAIL_USER=your_email@gmail.com
EMAIL_PASS=your_email_password

```

**Run Server:**

```bash
npm start
# Server runs on http://localhost:3001

```

### 3. AI Chatbot Service Setup (Python)

Navigate to the chatbot folder and install Python requirements.

```bash
cd ../backend_chatbot
pip install -r requirements.txt

```

**Run Service:**

```bash
python api.py
# Service runs on http://localhost:5000 (default Flask port)

```

### 4. Frontend Setup (React + Vite)

Navigate to the frontend folder.

```bash
cd ../vite-frontend
npm install

```

**Run Frontend:**

```bash
npm run dev
# Application usually runs on http://localhost:5173

```

---

## 📂 Project Structure

```
curely-v1/
├── backend/                 # Node.js/Express API
│   ├── config/              # DB connection
│   ├── models/              # Mongoose models (User, Appointment, Report, etc.)
│   ├── routes/              # API Routes (auth, doctor, lab, chat, etc.)
│   ├── uploads/             # Static folder for storing uploaded reports
│   └── server.js            # Entry point
│
├── backend_chatbot/         # Python Flask ML Service
│   ├── models/              # Pickle files for ML models
│   ├── api.py               # Flask entry point
│   └── model_utils.py       # Prediction logic
│
└── vite-frontend/           # React Frontend
    ├── src/
    │   ├── components/      # Reusable UI components
    │   ├── pages/           # Pages for different roles (Lab, Doctor, Customer)
    │   └── App.jsx          # Main routing logic
    └── package.json

```

## 🛡️ License

This project is licensed under the **ISC License**.
