# 🚀 Roommate Connect (Production Deployment)

RoommateConnect is a premium, real-time platform designed to bridge the gap between people offering rooms and those seeking them. Built with a focus on trust, aesthetics, and lightning-fast communication.

🌐 Live: https://roommate.jay26.online

## 🚀 Core Features

- **Dual-Mode Listings**: Switch between "Offering a Room" (Owners) and "Seeking a Room" (Renters).
- **Real-Time Chat**: Direct, instant messaging with image sharing and "View Once" media.
- **Smart Filters**: Advanced location-based search (States/Cities) and price range filtering.
- **Push Notifications**: Never miss a match or message with browser-level push alerts.
- **Admin Command Center**: Complete oversight with real-time banning, broadcast alerts, and activity analytics.
- **Premium UX**: Glassmorphism UI, Skeleton screens for smooth loading, and responsive design for all devices.

---

## 🧠 Overview

This project focuses not only on development but on real-world deployment and system design using DevOps practices.

---

## ⚙️ Tech Stack

- Frontend: React (Vite)
- Backend: Node.js (Express)
- Database: PostgreSQL
- DevOps: Docker, Jenkins
- Server: AWS EC2
- Proxy: NGINX
- DNS: Route53 / Domain

---

## 🏗️ Architecture

User → Domain → NGINX → Frontend (Docker)
                        ↓
                    Backend (Docker)
                        ↓
                  PostgreSQL

```mermaid
graph TD
    User((User))
    Admin((Admin))
    
    subgraph Frontend [React v18 + Vite]
        UI[Glassmorphism UI]
        Context[Auth / Socket / Push Contexts]
        Client[Axios API Client]
    end
    
    subgraph Realtime [WebSockets]
        WS[Socket.io Server]
    end
    
    subgraph Backend [Express.js Node Server]
        Auth[JWT Authentication]
        API[RESTful Endpoints]
        Logic[Admin & Room Logic]
    end
    
    subgraph Database [ORM + Storage]
        Prisma[Prisma ORM]
        DB[(SQLite / PostgreSQL)]
    end
    
    User <--> UI
    Admin <--> UI
    UI <--> Context
    Context <--> Client
    Client <--> API
    API <--> Logic
    Logic <--> Prisma
    Prisma <--> DB
    WS <--> Logic
    WS <--> Context
```

---

## 🔄 CI/CD Pipeline

GitHub → Jenkins → Docker Build → Deployment

- Automatic deployment on code update
- Containerized services
- Zero manual deployment

---

## 🔐 Deployment Features

- Custom domain setup
- HTTPS enabled (SSL)
- Reverse proxy using NGINX
- Environment-based configuration

---

## 🧪 Real-World Debugging Experience

Handled production-level issues:

- Backend crash due to DB failure
- NGINX downtime
- Docker container failures
- API misconfiguration
- High CPU usage

---

## 🧠 Linux Administration

- System monitoring (CPU, RAM, Disk)
- Service management (Docker, NGINX)
- Log analysis
- Incident handling
- Backup & maintenance

---

## ⚠️ Note

This is a production-level project.  
Full source code is private but available upon request.

---

## 📸 Screenshots
## Website UI
<img width="1364" height="595" alt="image" src="https://github.com/user-attachments/assets/74f3b712-e355-43f5-ad94-8dea270b2e1b" />

## Jenkins pipeline
<img width="895" height="348" alt="image" src="https://github.com/user-attachments/assets/7589fd32-ae51-4c7d-a9e5-6fe107612efc" />

## AWS EC2
<img width="1358" height="475" alt="image" src="https://github.com/user-attachments/assets/e9b3b88e-947b-48c1-b25f-cea3f8c910d9" />

## Terminal (docker ps)
<img width="1332" height="191" alt="image" src="https://github.com/user-attachments/assets/a924b345-10d3-40ad-bd1d-cdcf9e9b2e6b" />




---

## 📬 Contact

Open to feedback and collaboration.
