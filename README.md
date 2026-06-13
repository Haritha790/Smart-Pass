# 🚪 SmartPass – Gate Pass Management System

## 📖 Overview

SmartPass is a full-stack web application designed to simplify and digitize gate pass management in educational institutions. It allows students to request gate passes, wardens to approve or reject requests, and security personnel to verify and track student movement efficiently.

---

## ✨ Features

### 🎓 Student Module
- 📝 Apply for Gate Pass
- 📋 View Pass History
- 📊 Track Approval Status

### 👨‍💼 Admin (Warden) Module
- 👀 View All Requests
- ✅ Approve Requests
- ❌ Reject Requests
- 📈 Monitor Student Activity

### 🛡️ Security Module
- 🔍 Verify Pass Using Pass ID
- 🚶 Mark Student OUT
- 🏠 Mark Student IN
- 📌 View Currently Outside Students

---

## 🛠️ Tech Stack

### 🎨 Frontend
- React.js
- React Router
- CSS

### ⚙️ Backend
- Node.js
- Express.js

### 🗄️ Database
- MongoDB Atlas

### ☁️ Deployment
- Netlify (Frontend)
- Render (Backend)

---

## 📂 Project Structure

### 🎨 Frontend
```bash
src/
├── api/
│   └── smartpassAPI.js
├── pages/
│   ├── Login.jsx
│   ├── Register.jsx
│   ├── StudentDashboard.jsx
│   ├── AdminDashboard.jsx
│   └── SecurityDashboard.jsx
├── css/
│   └── styles
```

### ⚙️ Backend
```bash
backend/
├── models/
│   └── Pass.js
├── controllers/
│   ├── passController.js
│   └── securityController.js
├── routes/
│   ├── passRoutes.js
│   ├── authRoutes.js
│   └── securityRoutes.js
├── middleware/
│   └── authMiddleware.js
├── config/
│   └── db.js
└── server.js
```

---

## 🔄 How It Works

1. 📝 Student submits a gate pass request.
2. 📤 Request is sent to the backend API.
3. 🗄️ Data is stored in MongoDB Atlas.
4. 👨‍💼 Admin reviews the request.
5. ✅ Admin approves or ❌ rejects the request.
6. 🛡️ Security verifies the pass using Pass ID.
7. 🚶 Student movement is recorded as OUT and IN.

---

## 🔐 Authentication & Security

- 🔑 JWT Authentication
- 👤 Secure Login & Registration
- 🛡️ Protected Routes
- 📦 Token Storage in Local Storage
- 🔒 Role-Based Access Control

---

## 🗃️ Database Schema

```json
{
  "student": "ObjectId",
  "reason": "String",
  "date": "Date",
  "returnDate": "Date",
  "status": "pending | approved | rejected",
  "outTime": "Date",
  "inTime": "Date",
  "isCurrentlyOut": "Boolean"
}
```

---

## 🌐 API Endpoints

### 🔐 Authentication
```http
POST /api/auth/register
POST /api/auth/login
```

### 📝 Pass Management
```http
GET /api/passes
POST /api/passes
```

### 👨‍💼 Admin
```http
GET /api/passes/all
PATCH /approve
PATCH /reject
```

### 🛡️ Security
```http
POST /verify
POST /log
GET /status
```

---

## 🚀 Installation

### 📥 Clone the Repository

```bash
git clone https://github.com/your-username/SmartPass.git
cd SmartPass
```

### 📦 Install Dependencies

Frontend:
```bash
npm install
```

Backend:
```bash
cd backend
npm install
```

### ⚙️ Configure Environment Variables

Create a `.env` file inside the backend folder:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
PORT=5000
```

### ▶️ Run the Application

Frontend:
```bash
npm start
```

Backend:
```bash
cd backend
npm run dev
```

---

## 🚧 Challenges Faced

- 🌐 Handling CORS Issues
- 🔗 MongoDB Atlas Integration
- 🆔 Pass ID Generation Logic
- 🔐 Implementing Role-Based Authentication
- ☁️ Frontend & Backend Deployment

---

## 🔮 Future Enhancements

- 📧 Email Notifications
- 📱 SMS Alerts
- 📷 QR Code-Based Pass Verification
- 📊 Dashboard Analytics
- 📱 Mobile Application Support
- 🎯 Enhanced User Experience

---

## 🎯 Key Highlights

✅ Full-Stack Web Application  
✅ JWT Authentication  
✅ Role-Based Access Control  
✅ MongoDB Database Integration  
✅ Student, Admin & Security Dashboards  
✅ Responsive and User-Friendly Interface  

---

## 📸 Screenshots


<img width="692" height="857" alt="Screenshot 2026-06-13 232910" src="https://github.com/user-attachments/assets/5ee2c6ff-5bcf-4263-822c-96c49a479b47" />

<img width="695" height="842" alt="Screenshot 2026-06-13 232920" src="https://github.com/user-attachments/assets/de9c6eb7-666a-40d5-a191-d8294e2eaad4" />

<img width="1026" height="711" alt="Screenshot 2026-06-13 233207" src="https://github.com/user-attachments/assets/47cfbbfe-3845-4359-ab07-f357f48ad8b9" />

<img width="1903" height="857" alt="Screenshot 2026-06-13 233219" src="https://github.com/user-attachments/assets/f976754f-ee12-4cb6-81ae-e8c46e7f61ed" />


### 💡 "Making Campus Gate Pass Management Smarter, Faster, and More Secure."

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

---

## 👩‍💻 Author

**Haritha Bammidi**

GitHub: https://github.com/Haritha790 

Project Repository: https://github.com/Haritha790/Smart-Pass.git

Live Demo: https://smart-passs.netlify.app/



📧 Open to collaborations and opportunities.

⭐ If you found this project useful, consider giving it a star on GitHub!

---
