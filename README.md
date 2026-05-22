````md
# Production DevOps Project

Production-style Flask application deployment using AWS EC2, Docker, Gunicorn, Nginx, and Terraform.

---

# Project Overview

This project demonstrates a complete DevOps deployment workflow:

- Infrastructure provisioning with Terraform
- Flask application containerization using Docker
- Gunicorn as the WSGI application server
- Nginx reverse proxy configuration
- AWS EC2 deployment
- GitHub version control

---

# Tech Stack

- Python
- Flask
- Docker
- Gunicorn
- Nginx
- Terraform
- AWS EC2
- Git & GitHub

---

# Project Structure

```bash
production-devops-project/
│
├── app/
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
│
├── nginx/
│   └── default.conf
│
├── terraform/
│   ├── main.tf
│   ├── provider.tf
│   ├── outputs.tf
│   └── variables.tf
│
├── .gitignore
└── README.md
````

---

# Features

* Infrastructure as Code using Terraform
* Dockerized Flask application
* Reverse proxy setup with Nginx
* Production deployment architecture
* AWS EC2 hosting
* GitHub repository integration

---

# Deployment Workflow

## 1. Provision Infrastructure

```bash
cd terraform
terraform init
terraform apply
```

---

## 2. SSH into EC2

```bash
ssh -i your-key.pem ubuntu@your-ec2-public-ip
```

---

## 3. Run Docker Container

```bash
docker build -t flask-devops-app .
docker run -d -p 8000:5000 flask-devops-app
```

---

## 4. Configure Nginx

```bash
sudo vim /etc/nginx/sites-available/default
```

Nginx forwards incoming traffic from port 80 to the Flask application running on port 8000.

---

## 5. Restart Nginx

```bash
sudo systemctl restart nginx
```

---

# Application Access

Open in browser:

```text
http://your-ec2-public-ip
example:
http://3.27.250.196
```

---

# Learning Outcomes

This project helped me understand:

* Infrastructure provisioning with Terraform
* Linux server management
* Docker containerization
* Reverse proxy architecture
* Production deployment workflow
* GitHub project management
* Difference between local and remote environments

---

# Future Improvements

* GitHub Actions CI/CD pipeline
* HTTPS with SSL certificates
* Docker Compose
* Kubernetes deployment
* Monitoring and logging
* Auto-scaling infrastructure

---

# Author

Badal Senchury

```
```
