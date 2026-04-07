# 🚀 Django Notes App - CI/CD Pipeline with Jenkins & Docker

This project demonstrates an end-to-end DevOps workflow where a Django-based Notes Application is containerized and deployed using Docker, and the entire process is automated using a Jenkins CI/CD pipeline.

---

## 🔧 Project Overview

The goal of this project was to automate the complete application lifecycle — from code commit to deployment.

Initially, the application was deployed manually using Docker. Later, a Jenkins pipeline was implemented to automate the build, push, and deployment process.

---

## 🏗️ Architecture

GitHub → Jenkins Pipeline → Docker Build → Docker Hub → Deployment (Docker Compose)

---

## ⚙️ Tech Stack

- 🐍 Django (Backend)
- 🗄️ MySQL (Database)
- 🌐 Nginx (Reverse Proxy)
- 🐳 Docker & Docker Compose
- 🔁 Jenkins (CI/CD)
- 📂 GitHub (Version Control)

---

## 🔁 CI/CD Pipeline Stages

1. **Code Clone**
   - Pulls the latest code from GitHub repository

2. **Build**
   - Builds Docker image for Django app

3. **Push**
   - Tags and pushes the Docker image to Docker Hub

4. **Deploy**
   - Runs containers using Docker Compose

---

## 🔐 Jenkins Setup

- Installed Jenkins on local machine (Windows)
- Created a Pipeline job using Declarative Pipeline
- Configured Docker Hub credentials in Jenkins

**Credentials Used:**
- ID: `dockerHub`
- Type: Username & Password (Access Token recommended)

---

## 🌐 Webhook Integration

GitHub webhook is configured to trigger the Jenkins pipeline automatically on every push.

---

## 📦 Docker Setup

### Build Image
```bash
docker build -t notes-app:latest .
