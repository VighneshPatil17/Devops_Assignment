# DevOps Internship Assignment 🚀

This project demonstrates a complete DevOps setup using Docker Compose and Nginx as a reverse proxy. It orchestrates two microservices — one in Go and another in Python — both accessible through a single entry point via Nginx.

---

## 🧱 Project Structure

├── docker-compose.yml
├── nginx
│ ├── nginx.conf
│ └── Dockerfile
├── service_1
│ ├── Dockerfile
│ └── main.go
├── service_2
│ ├── Dockerfile
│ └── app.py
└── README.md


---

## 🎯 Objective

- Containerize two services (Golang and Python).
- Route incoming requests via Nginx based on path (`/service1`, `/service2`).
- Ensure everything is accessible at `http://localhost:8080`.

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd Assignment

2. Start the application

  docker-compose up --build

3. Access Services

 Service 1 (Go): http://localhost:8080/service1/hello

 Service 2 (Python): http://localhost:8080/service2/

🔁 How Routing Works
Nginx is configured as a reverse proxy:

| URL Path      | Routed To          |
| ------------- | ------------------ |
| `/service1/*` | Go (Service 1)     |
| `/service2/*` | Python (Service 2) |

Incoming requests are routed based on their path prefix using nginx.conf.


🔍 Logging & Monitoring

 All HTTP requests are logged with timestamps and URLs via Nginx.

 Health check endpoints (/ping) are available for both services.

You can check logs using:

 docker-compose logs


✅ Health Checks
 
 Each service has a /ping route:

 Service 1 → /service1/ping

 Service 2 → /service2/ping


✨ Bonus Features

 Clean, modular Docker setup.

 Internal bridge networking (no host-mode).

 Well-commented codebase.

 Structured logs with timestamps.


🧠 Technologies Used
 
 Docker

 Docker Compose

 Golang

 Python (Flask)

 Nginx (reverse proxy)

 Linux (Ubuntu base)


📌 Notes for Reviewers
The setup requires no external dependencies.

Easy to run, inspect, and extend.

Ideal demonstration of containerized microservices behind a single unified entry point.

🤝 Author
Made with passion by Vighnesh Patil — aspiring DevOps Engineer
🌐 GitHub: 


---

4. **Save and Exit in `vi`:**
   - Press `Esc`
   - Type `:wq`
   - Press `Enter`

That’s it! ✅

---

Let me know if you also want:
- A short **demo video script**
- GitHub description text
- Assistance pushing to GitHub

