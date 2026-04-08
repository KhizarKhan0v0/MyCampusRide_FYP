# 🚌 MyCampusRide - Smart Campus Transport Management System

MyCampusRide is a comprehensive MERN stack application designed to streamline campus transportation. It provides real-time bus tracking, route management, and seamless communication between students, drivers, and administrators.

## 🚀 Key Features

- **Real-time Tracking**: Live GPS-based bus location updates using Socket.io and Leaflet.
- **Role-based Dashboards**:
  - **Admin**: Manage users, buses, routes, and overall system status.
  - **Driver**: Start/end trips and broadcast live location.
  - **Student**: View available routes, track buses in real-time, and get notifications.
- **Smart Notifications**: Instant alerts for trip starts, completions, and campus updates.
- **Profile Management**: Profile picture uploads and personalized settings.

## 🛠️ Tech Stack

- **Frontend**: React.js, Vite, Material UI, Leaflet (Maps), Axios, Socket.io-client.
- **Backend**: Node.js, Express.js, MongoDB (Mongoose), Socket.io.
- **Auth**: JWT (JSON Web Tokens) with Secure HTTP-only cookies.
- **Storage**: Multer for image uploads.

---

## 💻 Local Setup Instructions

### Prerequisites
- Node.js (v16+)
- MongoDB (Running locally or on MongoDB Atlas)

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd MyCampusRide
```

### 2. Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the `backend` folder:
   ```env
   PORT=5001
   MONGO_URI=mongodb://localhost:27017/mycampusride
   JWT_SECRET=your_jwt_secret
   ADMIN_SECRET_CODE=your_admin_code
   FRONTEND_URL=http://localhost:3000
   ```
4. Start the server:
   ```bash
   npm run dev
   ```

### 3. Frontend Setup
1. Open a new terminal and navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the `frontend` folder:
   ```env
   VITE_API_URL=http://localhost:5001
   VITE_BACKEND_URL=http://localhost:5001
   VITE_GOOGLE_MAPS_API_KEY=your_key_here
   ```
4. Start the development server:
   ```bash
   npm run dev
   ```

---

## 🌐 Deployment

### Backend (Render)
- Deploy the `backend` folder as a **Web Service**.
- Add environment variables for `MONGO_URI`, `JWT_SECRET`, and `FRONTEND_URL`.

### Frontend (Vercel/Netlify)
- Deploy the `frontend` folder as a **Single Page Application**.
- Add environment variables for `VITE_API_URL`.
- **Note**: This project includes `vercel.json` and `_redirects` files to ensure proper routing on these platforms.

---

## 📂 Project Structure

```text
├── backend/
│   ├── controllers/    # API logic
│   ├── models/         # Database schemas
│   ├── routes/          # API endpoints
│   ├── services/       # Socket.io and helper services
│   └── server.js       # Entry point
├── frontend/
│   ├── src/
│   │   ├── components/ # Reusable UI components
│   │   ├── pages/      # Dashboard and feature views
│   │   ├── api/        # Axios configurations
│   │   └── services/   # Frontend business logic
│   └── public/         # Static assets
└── README.md
```

## 📝 License
Distributed under the MIT License.
