# 🧪 My AWS HomeLab Setup: Linux, Ubuntu & Windows VMs

Welcome to my cloud-based HomeLab! This repo documents how I built and configured virtual machines (VMs) on AWS EC2 using Amazon Linux, Ubuntu, and Windows.

---

## ☁️ Tools Used
- AWS EC2
- Amazon Console (GUI)
- MobaXterm / Remote Desktop
- SSH Keys
- Git & GitHub

---

## 🐧 Amazon Linux VM Setup

1. **Launch EC2 Instance**
   - AMI: Amazon Linux 2023
   - Type: `t3.micro` (Free Tier)
   - Key Pair: `Myhomelapproject.pem`

2. **Connect**
   ```bash
   ssh -i "Myhomelapproject.pem" ec2-user@<public-ip>

3. **Install Packages**
  - sudo yum update -y
  - sudo yum install httpd git -y

## 🐧 Ubuntu VM Setup
1. **Launch EC2 Instance**
  - AMI: Ubuntu 22.04 LTS
  - Type: t3.micro (Free Tier)
  - Key Pair: Myhomelapproject.pem

2. **Connect**
  - ssh -i "Myhomelapproject.pem" ubuntu@<public-ip>
  - Install Packages

3. **Install Packages**
  - sudo apt update && sudo apt upgrade -y
  - sudo apt install apache2 git -y

## 🪟 Windows VM Setup
1. **Launch EC2 Instance**
  - AMI: Windows Server 2022 Base
  - Download .pem key
2. **Get Administrator Password**
  - Decrypt with your .pem file from EC2 Console
3. **Connect Using RDP**
  -Use Remote Desktop with:
    makefile:
      Username: Administrator
      Password: <Decrypted Password>
