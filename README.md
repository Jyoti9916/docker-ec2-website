# 🚀 Dockerized Website Deployment on AWS EC2

## 📌 Project Overview

This project demonstrates how to deploy a static website using a Docker container on an AWS EC2 instance. The website is containerized using Docker and hosted on an Ubuntu EC2 server.

This project shows basic DevOps workflow including **Docker containerization, AWS cloud deployment, and GitHub version control**.

---

## 🛠️ Tools & Technologies

* AWS EC2 (Ubuntu Server)
* Docker
* Git
* GitHub
* Apache Web Server
* Linux Commands

---

## ⚙️ Implementation Steps

### 1️⃣ Launch AWS EC2 Instance

* Created Ubuntu EC2 instance
* Allowed **HTTP (Port 80)** in Security Group
* Connected to instance using SSH

---

### 2️⃣ Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
```

Verify Docker installation

```bash
docker --version
```

---

### 3️⃣ Clone Project from GitHub

```bash
git clone https://github.com/Jyoti9916/docker-ec2-website.git
cd docker-ec2-website
```

---

### 4️⃣ Create Dockerfile

```dockerfile
FROM ubuntu:latest
RUN apt update && apt install apache2 -y
COPY . /var/www/html
CMD ["apachectl","-D","FOREGROUND"]
```

---

### 5️⃣ Build Docker Image

```bash
docker build -t my-website .
```

---

### 6️⃣ Run Docker Container

```bash
docker run -d -p 80:80 my-website
```

This command maps container port **80** to EC2 server port **80**.

---

## 🌍 Output

After deployment, open browser and access:

```
http://YOUR-EC2-PUBLIC-IP
```

Example Output Page:

```
Docker Deployment Successful 🚀
Hosted on AWS EC2
Created by Jyoti
```
![Output](https://raw.githubusercontent.com/Jyoti9916/docker-ec2-website/main/output.PNG)
---

## 📂 Project Structure

```
docker-ec2-website
│
├── Dockerfile
├── index.html
└── README.md
```

---

## 🎯 Key Learning Outcomes

* Docker container creation
* Deploying applications on AWS EC2
* Running containers using Docker CLI
* Version control using GitHub
* Basic DevOps deployment workflow

---

## 👩‍💻 Author

**Jyoti**

GitHub Profile
https://github.com/Jyoti9916
