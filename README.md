
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

## 📂 Folder Structure
aws-autoscaling-apache-stack/
│
├── templates/
│ └── main.yaml # CloudFormation template
│
├── images/
│ └── architecture-diagram.png # AWS architecture
│ └── ... (screenshots)
│
│
└── README.md # This file


## 🔧 Deployment Steps

### 📍 1. Upload the Template to AWS CloudFormation

1. Go to AWS Console → CloudFormation → **Create Stack**
2. Choose **“With new resources (standard)”**
3. **Upload a template file** → `main.yaml`
4. Click **Next** and name your stack
5. Click through and **Create Stack**

### 📍 2. Wait for Stack Completion

- Watch for `CREATE_COMPLETE` in CloudFormation
- Go to **Outputs** tab → copy the **LoadBalancer DNS**

### 🌐 3. Access Apache in Browser

```text
http://<LoadBalancerDNS>

### 1. Clone the Repo
```bash
git clone https://github.com/YOUR_USERNAME/aws-autoscaling-apache-stack.git
cd aws-autoscaling-apache-stack
