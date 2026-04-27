# 🚀 Socket.IO Chat Backend

A simple real-time chat backend built with **Node.js**, **Express**, and **Socket.IO**.
This server allows clients to connect and exchange messages instantly.

---

## 📦 Tech Stack

* Node.js
* Express
* Socket.IO

---

## ⚙️ Features

* Real-time communication using WebSockets
* Broadcast messages to all connected clients
* Simple and lightweight server setup
* CORS enabled (allows all origins)

---

## 📁 Project Structure

```
.
├── node_modules/
├── package.json
├── package-lock.json
└── index.js
```

---

## 🚀 Getting Started

### 1. Clone the repository

```
git clone https://github.com/Abdelghfarsalah/socket-backend.git
cd socket-backend
```

### 2. Install dependencies

```
npm install
```

### 3. Run the server

```
node index.js
```

Server will run on:

```
http://localhost:3001
```

---

## 🔌 Socket Events

### 📥 Client → Server

* `send-message`
  Sends a message to the server

### 📤 Server → Client

* `new-message`
  Broadcasts message to all connected clients

---

## 🧪 Test the Server

You can test using:

* Postman (for HTTP route `/`)
* Browser → open `http://localhost:3001`
* Any frontend with Socket.IO client

---

## 📌 Example (Client Side)

```javascript
import { io } from "socket.io-client";

const socket = io("http://localhost:3001");

socket.emit("send-message", "Hello world!");

socket.on("new-message", (msg) => {
  console.log(msg);
});
```

---

## 📄 License

This project is open-source and free to use.
