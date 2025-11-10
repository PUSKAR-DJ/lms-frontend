# 🧩 **README — lms-frontend**

```markdown
# 🎓 LMS Frontend (React)

This is the **frontend** of the Learning Management System (LMS), built using **React + Vite**.  
It provides interfaces for **Students**, **Instructors**, and **Admins** to interact with the LMS backend.

---

## 🚀 Features

### 👨‍🎓 Student
- Login and profile view
- View enrolled courses, lessons, and grades
- View attendance percentage
- Pay course fees and download receipts
- Check daily class schedule
- Submit feedback

### 👩‍🏫 Instructor
- Login to manage assigned courses
- Upload lessons, materials, and assignments
- Mark attendance for students
- View and grade submissions
- View schedules

### 🧑‍💼 Admin
- Create and manage users, courses, and departments
- Create class schedules
- View reports and analytics
- Monitor attendance, fees, and grades

---

## ⚙️ Tech Stack

| Layer | Technology |
|--------|-------------|
| Frontend Framework | React + Vite |
| UI Styling | TailwindCSS / Material UI |
| State Management | Context API / Redux Toolkit |
| Routing | React Router v6 |
| HTTP Client | Axios |
| Authentication | JWT stored in localStorage |
| Environment Config | Vite `.env` variables |

---

## 🧱 Project Structure

```

src/
├── components/        # Reusable UI components
├── pages/             # Pages for different routes
├── context/           # Auth & role-based context providers
├── services/          # Axios API service wrappers
├── router/            # Protected route logic
├── App.jsx            # Main application routes
└── main.jsx           # Entry point

````

---

## 🔧 Setup Instructions

### 1️⃣ Clone the Repo
```bash
git clone https://github.com/PUSKAR-DJ/lms-frontend.git
cd lms-frontend
````

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Configure Environment

Create a `.env` file in the root:

```
VITE_API_URL=http://localhost:5000/api
```

### 4️⃣ Run Development Server

```bash
npm run dev
```

### 5️⃣ Build for Production

```bash
npm run build
```

---

## 🔗 API Integration

The frontend communicates with the backend via RESTful APIs.
Example:

```js
import axios from "axios";

const API = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
});

export const loginUser = (data) => API.post("/auth/login", data);
```

---

## 🧩 Role-based Routing Example

```jsx
<Route
  path="/dashboard"
  element={
    userRole === "Admin"
      ? <AdminDashboard />
      : userRole === "Instructor"
      ? <InstructorDashboard />
      : <StudentDashboard />
  }
/>
```

---

## 💡 Future Enhancements

* Add charts for grade analytics
* Support push notifications
* Multi-language localization
* Dark mode toggle

---

## 🧑‍💻 Contributors

* [Raj Sharma](https://github.com/rajsha10)
* [Pronay Sarkar](https://github.com/PronaySarkar)
* [Subhadip Mandal](https://github.com/Subhadip1001)
* [Puskar Saha](https://github.com/PUSKAR-DJ)

---
