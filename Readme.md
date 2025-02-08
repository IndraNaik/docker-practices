# 🐳 Docker Practices  

This repository contains **Docker concepts, best practices, and real-world examples** to help you master containerization.  

## 🏛 Repository Structure  

📂 **Dockerfiles/** → Sample Dockerfiles for different languages and frameworks.  
📂 **Docker-Compose/** → Multi-container application setups.  
📂 **CI-CD/** → GitHub Actions and GitLab CI/CD for Docker automation.  
📂 **Security/** → Secure Dockerfile practices and vulnerability scanning.  
📂 **Kubernetes/** → Kubernetes manifests and Helm charts.

---

# 📌 Docker Concepts & Best Practices 🚀  

## 1️⃣ What is Docker?  
Docker is a computer program that performs **operating-system-level virtualization**, also known as **"containerization"**.

### 🔹 Why Use Docker?  
✅ Works on **any environment** (Mac, Windows, Linux).  
✅ **Lightweight & Fast** compared to Virtual Machines.
✅ Simplifies deployment and management of **microservices**.  
✅ **Portable**: Runs anywhere with Docker installed.  
✅ Avoids compatibility issues (**"Works on my machine!"** problem).  

---
## 2️⃣ Dockerfile vs Docker Image vs Docker Container  
| Feature          | Dockerfile | Docker Image | Docker Container |
|-----------------|------------|--------------|------------------|
| Definition      | A script containing instructions to build a Docker image. | A snapshot of an application and its dependencies. | A running instance of a Docker image. |
| Purpose        | Defines the environment and dependencies. | Used to create containers. | Runs the application in an isolated environment. |
| State         | Text file | Static (read-only) | Dynamic (running process) |
| Persistence  | Exists as a file | Stored in a registry | Temporary or persistent (depending on setup) |
| Example       | `Dockerfile` | `ubuntu:latest` | Running instance of `ubuntu:latest` |

---

## 3️⃣ How Does Docker Work?  
Docker follows a **client-server architecture**:  

🔹 **Docker CLI** → User interacts using `docker` commands.  
🔹 **Docker Daemon** → Runs in the background and manages containers.  
🔹 **Docker Images** → Prebuilt snapshots of applications.  
🔹 **Docker Containers** → Running instances of images.  

---

## 4️⃣ Installing Docker  
### 🔹 Requirements  
✔ Windows 10/11, macOS, or Linux.  
✔ Enable **Virtualization in BIOS** (for Windows).  

### 🔹 Installation Steps  
#### 🖥 Windows & macOS  
Download and install **Docker Desktop** from [Docker Official Site](https://www.docker.com/products/docker-desktop).  

#### 💻 Linux  
Install via terminal:  
```bash  
sudo apt-get update  
sudo apt-get install docker.io
sudo apt-get install docker-compose
docker --version  
```

---

## 5️⃣ Essential Docker Commands  
```bash  
docker pull <image_name>   # Pulls the image from DockerHub
docker run hello-world     # Run a test container  
docker images              # List downloaded images  
docker ps                  # Show running containers  
docker ps -a               # Show all containers (stopped + running)  
docker stop <container_id> # Stop a running container  
docker rm <container_id>   # Remove a container  
docker rmi <image_id>      # Remove an image
docker image prune -a      # Remove all unused images, containers, networks
```

---

🚀 **Stay tuned for more Docker best practices and real-world examples!**
