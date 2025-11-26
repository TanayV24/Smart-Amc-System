<div align="center">

# 🏢 Smart AMC System

### Comprehensive AMC (Annual Maintenance Contract) Management Platform

![NodeJS](https://img.shields.io/badge/Node.js-18.x-43853D?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-Framework-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Database-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react&logoColor=white)

**A full-stack system built to manage clients, devices, service schedules, contracts, and AMC renewals with a clean UI and scalable backend architecture.**

[🐛 Report Bug](https://github.com/TanayV24/Smart-Amc-System/issues) | [💡 Request Feature](https://github.com/TanayV24/Smart-Amc-System/issues)

</div>

---

## ✨ Features

### 🧑‍💼 **Business Features**
- 👥 **Client Management** – Add, edit, and track all clients  
- 🖥️ **Device Tracking** – Register devices under AMC with details  
- 📅 **Maintenance Scheduling** – Auto-schedule and track AMC visits  
- 🧾 **Contract Management** – Manage AMC contracts, validity & renewals  
- 📊 **Service Logs** – View full maintenance history for each device  
- 💰 **Invoice & Billing Records** – Track AMC payments and renewals  

### 🔧 **Technical Features**
- ⚡ **RESTful API** – Clean Express backend  
- 🧱 **Modular MVC Structure** – Controllers, models, routes cleanly separated  
- 🗄 **MongoDB Database** – Scalable document-based storage  
- 🌐 **Optional Frontend (React)** – Clean UI for AMC dashboard  
- 🚀 **High Scalability** – Add staff roles, authentication, more modules easily  

---

## 🛠 Tech Stack

<table>
<tr>
<td width="50%" valign="top">

### Backend
- **Runtime:** Node.js  
- **Framework:** Express.js  
- **Database:** MongoDB / Mongoose  
- **API Architecture:** REST  
- **Utilities:** bcrypt, JWT (optional), dotenv  

</td>
<td width="50%" valign="top">

### Frontend (If included)
- **Framework:** React  
- **UI Styling:** CSS / Tailwind / Custom Components  
- **State Management:** Hooks  
- **HTTP Client:** Axios  

</td>
</tr>
</table>

---

## 📋 Prerequisites

Install the following tools:

| Tool | Version | Link |
|------|---------|------|
| 🟢 Node.js | 16+ | https://nodejs.org |
| 📦 npm | Latest | Comes with Node |
| 🍃 MongoDB | Latest | https://www.mongodb.com |
| 💻 Git | Latest | https://git-scm.com |

Check installation:

```

node --version
npm --version
mongo --version
git --version

```

---

## ⚙️ Installation & Setup

### 🚀 Quick Start

### 1. Clone the project
```

git clone [https://github.com/TanayV24/Smart-Amc-System.git](https://github.com/TanayV24/Smart-Amc-System.git)
cd Smart-Amc-System

```

---

### 2. Backend Setup
```

cd backend
npm install

```

Create `.env`:
```

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret

```

Run backend:
```

npm run dev

```

Backend runs at:  
➡️ `http://localhost:5000`

---

### 3. Frontend Setup (if included)
```

cd ../frontend
npm install
npm run dev

```

Frontend runs at:  
➡️ `http://localhost:3000`

---

## 🎮 How to Use

1. Start backend (port 5000)  
2. Start frontend (port 3000)  
3. Open `http://localhost:3000`  
4. Add clients  
5. Register their devices  
6. Create AMC contracts  
7. Track maintenance schedule  
8. View service logs & invoices  

Perfect for IT service companies or freelancers handling hardware maintenance.

---

## 📁 Project Structure

```

Smart-Amc-System/
│
├── backend/                  # Express Backend
│   ├── controllers/          # Business logic
│   ├── models/               # Mongoose models
│   ├── routes/               # API routes
│   ├── config/               # DB config & environment
│   ├── utils/                # Helper functions
│   ├── middleware/           # Auth, validation (optional)
│   ├── server.js             # Backend entry point
│   └── package.json
│
├── frontend/ (optional)      # React Frontend
│   ├── public/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── services/
│   │   ├── App.jsx
│   │   └── index.css
│   ├── package.json
│
├── .gitignore
└── README.md

````

---

## 🔧 API Endpoints (Backend)

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/api/clients` | Add a new client |
| `GET` | `/api/clients` | Get all clients |
| `POST` | `/api/devices` | Register a device |
| `GET` | `/api/devices/:clientId` | Get devices for a client |
| `POST` | `/api/amc` | Create AMC contract |
| `GET` | `/api/amc/:clientId` | Get AMC details |
| `POST` | `/api/maintenance` | Add maintenance log |
| `GET` | `/api/maintenance/:deviceId` | View service history |

Example:
```js
axios.post("http://localhost:5000/api/clients", {
  name: "ABC Pvt Ltd",
  address: "Mumbai",
  contact: "9876543210"
});
````

---

## 🐛 Troubleshooting

<details>
<summary>MongoDB not connecting</summary>

Check your `.env` MONGO_URI value.

Try:

```
mongosh
```

If MongoDB shell opens, DB is working.

</details>

<details>
<summary>Backend crashes on start</summary>

Run:

```
npm install
node server.js
```

Ensure Node ≥ 16.

</details>

<details>
<summary>Frontend not loading data</summary>

Confirm API URL is correct in your frontend service config.

</details>
