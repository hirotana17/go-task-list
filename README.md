# Go Task List - Full Stack Todo Application

A modern, full-stack todo application built with Go (Fiber) backend and React (Vite) frontend, featuring real-time task management with MongoDB integration.

![Go Task List](https://img.shields.io/badge/Go-1.23.7+-blue?logo=go)
![React](https://img.shields.io/badge/React-19.1.0-blue?logo=react)
![MongoDB](https://img.shields.io/badge/MongoDB-6.0+-green?logo=mongodb)
![TypeScript](https://img.shields.io/badge/TypeScript-5.8.3-blue?logo=typescript)

## 🚀 Features

- ✅ Create, view, complete, and delete tasks
- ✅ Real-time updates with React Query
- ✅ Modern UI with Chakra UI
- ✅ Hot reload for development

## 🛠️ Tech Stack

**Backend**: Go, Fiber, MongoDB  
**Frontend**: React, TypeScript, Vite, Chakra UI  
**Development**: Air (hot reload), React Query

## 📋 Prerequisites

- **Go 1.23.7+** - [Download here](https://golang.org/dl/)
- **Node.js 18+** - [Download here](https://nodejs.org/)
- **MongoDB** - Local or MongoDB Atlas

## 🚀 Quick Start

### 1. Clone and Setup

```bash
git clone https://github.com/hirotana17/go-task-list.git
cd go-task-list
```

### 2. Environment Variables

Create `.env` file:
```bash
MONGODB_URI=mongodb://localhost:27017
PORT=4000
ENV=development
```

**For MongoDB Atlas**: Replace with your connection string

### 3. Install Dependencies

```bash
# Backend
go mod tidy

# Frontend
cd client/vite-project
npm install
cd ../..
```

### 4. Start MongoDB

**Local MongoDB**:
```bash
brew install mongodb-community
brew services start mongodb-community
```

**Docker**:
```bash
docker run -d -p 27017:27017 --name mongodb mongo:latest
```

### 5. Run Application

**Terminal 1 - Backend**:
```bash
air
```

**Terminal 2 - Frontend**:
```bash
cd client/vite-project
npm run dev
```

### 6. Access

- **Frontend**: http://localhost:5173
- **Backend API**: http://localhost:4000

## 🔧 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/todos` | Get all todos |
| POST | `/api/todos` | Create todo |
| PATCH | `/api/todos/:id` | Complete todo |
| DELETE | `/api/todos/:id` | Delete todo |

## 🐛 Common Issues

**Port 4000 in use**:
```bash
lsof -ti:4000 | xargs kill -9
```

**MongoDB not running**:
```bash
brew services start mongodb-community
```

**Homebrew not installed**:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.