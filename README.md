
# AWS Auto Scaling Apache Stack

This project deploys an Apache Web Server using EC2, Auto Scaling Group, and Application Load Balancer via AWS CloudFormation.

## 🧱 Architecture
![Architecture](images/00-architecture-diagram.png)

## 🚀 What This Stack Includes

- ✅ **VPC & Subnets** (pre-existing)
- ✅ **Key Pair** created via CloudFormation (note: cannot SSH into instances)
- ✅ **Security Groups** for EC2 and ALB
- ✅ **Launch Template** with Apache2 installation via `UserData`
- ✅ **Auto Scaling Group** (Min: 1, Max: 2)
- ✅ **Application Load Balancer** (ALB) with Target Group and Health Checks
- ✅ **Public Subnets** for EC2 placement

## 🚀 Components
- Launch Template
- EC2 Ubuntu with Apache
- Application Load Balancer (ALB)
- Auto Scaling Group
- Security Groups
- KeyPair

## 🔧 Deployment Steps

### 1. Clone the Repo
```bash
git clone https://github.com/YOUR_USERNAME/aws-autoscaling-apache-stack.git
cd aws-autoscaling-apache-stack
