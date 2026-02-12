# 🚀 Terraform AWS 3-Tier Architecture

This project provisions a highly available, scalable, and production-ready 3-Tier architecture on AWS using Terraform.

---

## 🏗️ Architecture Overview

The infrastructure includes:

- VPC
- Public & Private Subnets (Multi-AZ)
- Internet Gateway
- Application Load Balancer (ALB)
- Auto Scaling Group (EC2 Web Tier)
- RDS MySQL (Private DB Tier)
- Security Groups
- Launch Template

---

## 📌 Architecture Diagram

Web Tier (Public Subnets)
    |
Application Load Balancer
    |
Auto Scaling EC2 Instances
    |
Database Tier (Private Subnets)
    |
Amazon RDS (MySQL)

---

## ☁️ AWS Services Used

- Amazon VPC
- EC2
- Auto Scaling
- Application Load Balancer
- RDS (MySQL)
- Security Groups
- Subnet Groups

---

## 📂 Project Structure

terraform-aws-3tier-architecture/
│
├── backend.tf
├── provider.tf
├── versions.tf
├── variables.tf
├── terraform.tfvars
├── outputs.tf
│
├── modules/
│   ├── vpc/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   │
│   ├── security-groups/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   │
│   ├── ec2/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   │
│   ├── alb/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── outputs.tf
│   │
│   └── rds/
│       ├── main.tf
│       ├── variables.tf
│       └── outputs.tf
│
└── README.md

