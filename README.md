# Docker Nginx Deployment on AWS EC2

A simple web application deployed using Docker on an AWS EC2 Ubuntu instance.

![Nginx Welcome Page](https://i.imgur.com/your-screenshot-link.png)  
*(Replace with your actual screenshot)*

## 🚀 Live Demo
**Public URL:** [http://13.233.255.154](http://13.233.255.154)

---

## ✅ Project Goal
Deploy a Docker-based web application on a cloud virtual machine (AWS EC2).

### Requirements Fulfilled:
- ✅ Installed Docker on Ubuntu EC2 instance
- ✅ Ran Nginx container
- ✅ Exposed container port to the internet
- ✅ Publicly accessible web application

---

## 🛠️ Technologies Used
- **AWS EC2** (Ubuntu)
- **Docker**
- **Nginx** (Official Docker Image)

---

## 📋 Steps Performed

### 1. Connect to EC2 Instance
```bash
cd ~/Downloads
ssh -i "dockers-key.pem" ubuntu@13.233.255.154
sudo apt update -y
sudo apt install -y docker.io
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ubuntu
docker run -d --name my-nginx -p 80:80 nginx
