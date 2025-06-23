# 🏗️ Three-Tier Web Application on AWS

This project demonstrates a production-like **three-tier architecture** on AWS using:

- **VPC** with public and private subnets
- **Bastion Host** for secure SSH access
- **EC2 Web Server** running Apache and PHP
- **RDS MySQL Database** in private subnet
- **Application Load Balancer** to expose the app
- **Security Groups** for secure traffic flow

---

## 📸 Architecture Diagram

![Architecture](images/vpc-setup.png)

---

## ✅ Project Steps

### 1. VPC & Subnet Setup
- Created VPC, public/private subnets, IGW, and route tables

![VPC Setup](images/vpc-setup.png)

### 2. Bastion & Web EC2 Instances
- Bastion in public subnet
- Web server in private subnet with Apache + PHP

![Bastion EC2](images/ec2-bastion.png)
![Web EC2](images/ec2-web-server.png)

### 3. Application Load Balancer
- Routes traffic to web EC2s
- Health checks configured

![ALB Config](images/alb-config.png)

### 4. RDS Database
- MySQL DB in private subnet
- Connected to app using PHP

![RDS Setup](images/rds-setup.png)

### 5. Deployed App
- Sample PHP form connected to RDS

![App Running](images/app-running.png)

---

## 🧹 Cleanup

- All resources terminated to avoid charges:
  - EC2, RDS, ALB, VPC, Elastic IPs, etc.

![Cleanup](images/cleanup-confirmation.png)

---

## 🧠 What I Learned

- Core AWS Networking (VPC, subnets, IGW)
- Bastion & private access via security groups
- Load balancing with ALB
- MySQL RDS deployment & EC2 connection
- Safe deletion to stay under Free Tier

---

## 📚 Tech Stack

- AWS (VPC, EC2, ALB, RDS)
- Apache, PHP, MySQL
- Linux (Amazon Linux 2)
- SSH + Bastion Architecture

---


