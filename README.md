# 🚀 DevOps CI/CD Automation Project

A complete End-to-End CI/CD Pipeline built using Jenkins, Docker, Docker Hub and AWS EC2.

---

## 📌 Project Overview

This project demonstrates an automated CI/CD pipeline for deploying a Python Flask application.

Whenever code is pushed to GitHub, Jenkins automatically:

- Pulls the latest source code
- Builds a Docker image
- Pushes the image to Docker Hub
- Deploys the latest container on AWS EC2

The application is available live without any manual deployment.

---

# 🏗 Project Architecture

```
Developer
    │
    ▼
GitHub Repository
    │
    ▼
Jenkins Pipeline
    │
    ▼
Docker Build
    │
    ▼
Docker Hub
    │
    ▼
AWS EC2
    │
    ▼
Live Flask Application
```

---

# 🛠 Technology Stack

| Technology | Purpose |
|------------|---------|
| Python Flask | Web Application |
| Docker | Containerization |
| Jenkins | CI/CD Automation |
| Git & GitHub | Source Code Management |
| Docker Hub | Image Registry |
| AWS EC2 | Deployment Server |
| Ubuntu 24.04 LTS | Operating System |

---

# ⚙ Jenkins Pipeline Stages

- ✅ Checkout Source Code
- ✅ Clone Repository
- ✅ Build Docker Image
- ✅ Push Image to Docker Hub
- ✅ Deploy Docker Container
- ✅ Post Build Actions

---

# 📂 Project Structure

```
ci-cd-project
│
├── templates
│     └── index.html
│
├── app.py
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
├── README.md
└── .gitignore
```

---

# 🚀 Pipeline Flow

```
GitHub
   │
   ▼
Jenkins
   │
   ▼
Docker Build
   │
   ▼
Docker Hub
   │
   ▼
AWS EC2
   │
   ▼
Live Application
```

---

# 🌐 Live Application

```
http://YOUR-EC2-PUBLIC-IP:5000
```

Example

```
http://13.233.146.167:5000
```

---

# 📷 Project Screenshots

### Jenkins Pipeline

(Add Screenshot)

---

### Jenkins Dashboard

(Add Screenshot)

---

### Docker Container

(Add Screenshot)

---

### Live Application

(Add Screenshot)

---

# 💻 Clone Repository

```bash
git clone https://github.com/noormohammad161996-cloud/ci-cd-project.git
```

---

# ▶ Run Locally

Install dependencies

```bash
pip install -r requirements.txt
```

Run

```bash
python app.py
```

Open

```
http://localhost:5000
```

---

# 🐳 Docker Commands

Build Image

```bash
docker build -t ci-cd-project .
```

Run Container

```bash
docker run -d -p 5000:5000 ci-cd-project
```

---

# 👨‍💻 Developed By

**Noor Mohammad**

DevOps Engineer

### Skills

- AWS
- Docker
- Jenkins
- Git & GitHub
- Linux
- Python Flask
- CI/CD
- Docker Hub

---

⭐ If you like this project, don't forget to Star the repository.