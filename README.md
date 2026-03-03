
# Dockerized Website Deployment on AWS EC2

## 📌 Project Overview
This project demonstrates deployment of a static website using Docker container on AWS EC2.

## 🛠️ Tools & Technologies
- AWS EC2 (Ubuntu)
- Docker
- GitHub
- Apache Web Server

## ⚙️ Implementation Steps

### 1. Install Docker
sudo apt update && sudo apt install docker.io -y

### 2. Clone Repository
git clone https://github.com/Jyoti9916/my-simple-website.git

### 3. Create Docker Image
docker build -t my-website .

### 4. Run Container
docker run -d -p 80:80 my-website

## 🌍 Output
Website successfully deployed using Docker on AWS EC2.

## 👩‍💻 Author
Jyoti  
🔗 https://github.com/Jyoti9916
