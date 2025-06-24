# 🔀 Multi-Service Reverse Proxy Project (Go + Python + Nginx)

This project demonstrates how to run two backend services — one written in Go and another in Python (FastAPI) — behind a single port using **Nginx** as a reverse proxy and **Docker Compose** for orchestration.

---

## 🧱 Services Overview

| Service   | Language | Port  | Route Prefix      |
|-----------|----------|-------|-------------------|
| Service 1 | Go       | 8001  | `/service1`       |
| Service 2 | FastAPI  | 8002  | `/service2`       |
| Nginx     | N/A      | 8080  | Routes traffic    |

---

## 🔧 How It Works

- **Nginx** listens on port `8080`
- Routes:
  - `/service1/*` → Go backend
  - `/service2/*` → FastAPI backend
- Everything is containerized via **Docker**

---

## 🚀 Run the Project

```bash
docker-compose up --build


Then open in your browser:

http://localhost:8080/service1/hello

http://localhost:8080/service2/hello

