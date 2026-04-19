# 🚀 CloudScale – Production-Grade AWS Auto Scaling Infrastructure

A complete end-to-end DevOps project demonstrating scalable, secure, and automated cloud infrastructure using AWS and CI/CD.

---

## 📌 Project Overview

This project implements a **highly available and scalable web application** using AWS services such as EC2, Auto Scaling, Load Balancer, Route 53, and ACM, along with CI/CD automation using GitHub Actions.

---

## 🏗️ Architecture
               ┌───────────────┐
               │     User      │
               │ (Browser)     │
               └──────┬────────┘
                      │
                      ▼
            ┌───────────────────┐
            │   Route 53 (DNS)  │
            └────────┬──────────┘
                     │
                     ▼
    ┌────────────────────────────────┐
    │ Application Load Balancer (ALB)│
    │        HTTPS (443)             │
    └──────────────┬─────────────────┘
                   │
     ┌─────────────┴─────────────┐
     │                           │
     ▼                           ▼
---

## ⚙️ Technologies Used

- AWS EC2
- Auto Scaling Group (ASG)
- Application Load Balancer (ALB)
- Route 53 (DNS)
- AWS Certificate Manager (ACM)
- CloudWatch (Monitoring)
- SNS (Alerts)
- GitHub Actions (CI/CD)
- Linux (Amazon Linux)
- Apache (httpd)

---

## 🚀 Features Implemented

### 🔹 Infrastructure
- Launched EC2 instances with automated setup using User Data
- Created AMI and Launch Template for reusable configurations
- Configured Auto Scaling Group for dynamic scaling
- Integrated Application Load Balancer for traffic distribution

### 🔹 Production Setup
- Configured custom domain using Route 53
- Enabled HTTPS using SSL certificate (ACM)

### 🔹 Monitoring
- Created CloudWatch alarms for CPU utilization
- Configured SNS for alert notifications

### 🔹 CI/CD
- Implemented GitHub Actions workflow
- Automated deployment to EC2 on every code push

---

## 🔁 CI/CD Workflow

1. Developer pushes code to GitHub
2. GitHub Actions workflow triggers
3. SSH into EC2 instance
4. Pull latest code (`git pull`)
5. Restart Apache server
6. Website updates automatically

---

## 🧪 Testing Performed

- Verified load balancing using ALB DNS
- Simulated high CPU usage using `stress` command
- Tested auto-healing by terminating instances
- Validated HTTPS with SSL certificate
- Tested CI/CD by pushing updates to GitHub

---

## 🐞 Issues Faced & Fixes

| Issue | Solution |
|------|---------|
| Load Balancer timeout | Fixed Security Group rules |
| DNS not resolving | Corrected nameserver configuration |
| SSL pending validation | Fixed Route 53 CNAME records |
| SSH permission denied | Used correct `.pem` key and permissions |
| CI/CD deployment issues | Fixed GitHub secrets and permissions |

---



## 🎯 Key Learnings

- Real-world troubleshooting of AWS infrastructure
- Understanding of DNS and SSL validation
- CI/CD automation using GitHub Actions
- Importance of monitoring and alerting

---

## 💼 Use Case

This project simulates a **real production environment** where applications must be:
- Highly available
- Secure (HTTPS)
- Scalable
- Automatically deployable

---

## 👩‍💻 Author

**Shabin Shareefa**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub!
