# Full Stack Chat Application

## 🚀 Introduction

Welcome to the Full Stack Chat Application! This project is designed to deliver a seamless real-time messaging experience while ensuring security and scalability. Built with modern technologies, it provides a robust foundation for real-time communication.

---

## 🔄 Workflow Overview

### 1⃣ User Interaction
Users interact with the frontend application to perform actions like logging in, sending messages, and navigating through the chat interface.

### 2⃣ Frontend (React + TailwindCSS)
- Renders the user interface and handles user inputs.
- Communicates with the backend using HTTP requests (REST API) and WebSockets (real-time messaging).

### 3⃣ Backend (Node.js + Express + Socket.io)
- Handles server-side logic, including authentication, message storage, and API processing.
- Uses Socket.io to enable real-time two-way communication.

### 4⃣ Database (MongoDB)
- Stores user profiles, chat messages, and other relevant data.
- Facilitates data retrieval, updates, and deletions via the backend API.

---

## ✨ Features

✔️ **Real-Time Messaging** – Instant communication powered by Socket.io.  
✔️ **Secure Authentication** – User access is secured with JWT authentication.  
✔️ **Scalable Architecture** – Designed for high traffic and data volume.  
✔️ **Modern UI** – Built with React and styled using TailwindCSS & DaisyUI.  
✔️ **Profile Management** – Users can upload and update profile pictures.  
✔️ **Online Status** – Track online/offline status of users in real time.  

---

## 🛠️ Tech Stack

### **Frontend**
- React
- TailwindCSS
- DaisyUI
- Zustand (State Management)

### **Backend**
- Node.js
- Express.js
- Socket.io
- MongoDB

### **DevOps & Deployment**
- Docker (Containerization)
- Kubernetes (Planned for Orchestration)
- Nginx (Web Server)

---

## 📝 Prerequisites
Ensure you have the following installed before setting up the project:
- **Node.js** (v14 or higher)
- **Docker** (for containerization)
- **Git** (to clone the repository)

---

## 🛠️ Setup & Configuration

### 1⃣ Clone the Repository
```sh
 git clone https://github.com/your-username/full-stack_chatApp.git
 cd full-stack_chatApp
```

### 2⃣ Set Up Environment Variables
Navigate to the backend directory and create a `.env` file:
```sh
cd backend
touch .env
```
Add the following details (modify as needed):
```env
MONGODB_URI=mongodb://mongoadmin:secret@mongodb:27017/dbname?authSource=admin
JWT_SECRET=your_jwt_secret_key
PORT=5001
```

> ⚠️ Replace `your_jwt_secret_key` with a strong secret key.

---

## 🏷️ Running the Application

### 💀 Using Docker Compose
```sh
 docker-compose up -d --build
```
Access the application:
- **Frontend:** `http://localhost`
- **Backend API:** `http://localhost:5001`

### 🏷️ Manual Setup with Docker

#### 1⃣ Create a Docker Network
```sh
 docker network create full-stack
```

#### 2⃣ Build & Run the Frontend
```sh
 cd frontend
 docker build -t full-stack_frontend .
 docker run -d --network=full-stack -p 5173:5173 --name frontend full-stack_frontend:latest
```
> The frontend is now accessible on **port 5173**.

#### 3⃣ Run MongoDB Container
```sh
 docker run -d -p 27017:27017 --name mongo mongo:latest
```

#### 4⃣ Build & Run the Backend
```sh
 cd backend
 docker build -t full-stack_backend .
 docker run -d --network=full-stack --add-host=host.docker.internal:host-gateway -p 5001:5001 --env-file .env full-stack_backend
```

### 🔍 Verify Connection
```sh
 docker-compose logs -f
```

---
## 📷 Screenshots

![Login Page](images/login%20page.png)
![Home Page](images/home%20page.png)
![Profile Page](images/profile.png)
![Chat App UI](images/ui.png)

---
## 🤝 Contributing

We welcome contributions from developers of all levels! Here’s how you can help:

🛠 **Report Issues:** Found a bug? Open an issue and describe it in detail.  
💡 **Suggest Features:** Have an idea to enhance the app? Let’s discuss it!  
🚀 **Submit Pull Requests:** Contribute fixes and new features—make sure to follow best practices.

---

## 🌍 Join Our Community

If you find this project useful, consider supporting it:
🌟 **Star the repo** to show your appreciation!  
🔄 **Fork it** and make improvements.  
🐛 **Report issues** and suggest new features.  
👨‍💻 **Contribute code** via pull requests.

---

## 🔮 Future Enhancements

✅ **CI/CD Pipelines:** Automate testing and deployment.  
✅ **Kubernetes Support:** Deploy on AWS/GCP/Azure with K8s manifests.  
✅ **Feature Expansion:** Add group chats, media sharing, and user status updates.

Stay tuned for more updates as we continue to enhance this project! 🚀
Connect with me on LinkedIn: [www.linkedin.com/in/mpdhanveerprakash](www.linkedin.com/in/mpdhanveerprakash)


Credits: @iemafzalhassan (Md. Afzal Hassan Ehsani) for creating this wonderful project repo.
