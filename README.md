# ☁️ Cloud HomeLab Setup (Amazon Free Tier)
![VM Setup Diagram](images/diagram.png)

A hands-on guide of how I built and secured a home lab using AWS Free Tier with Amazon Linux, Ubuntu, and Windows VMs.

---

## 🔧 What's Included

- ✅ Free-tier AWS account setup
- 👤 IAM: Users, Groups, and Permissions (CIA-based)
- 🔐 MFA configuration
- 💸 Cost alarm setup to avoid surprise charges
- 🧠 EC2: Deploying Amazon Linux, Ubuntu, and Windows
- 💻 Working with MobaXterm
- 🛠️ Tools installed: Nmap, Wireshark, Hydra
- ⚠️ Importance of stopping unused instances
- 🛡️ Security: MFA, least privilege, and alerts

---

## 📁 Directory Guide

- **`amazon-linux/`** – Step-by-step setup of Amazon Linux instance
- **`ubuntu/`** – Ubuntu instance and Hydra usage
- **`windows/`** – Windows instance and tools installed
- **`security/`** – IAM, MFA, cost control and instance shutdown practices
- **`resources/`** – External tools and useful links

---

## 🗃️ Example VMs

| VM Type        | Purpose                     | Tools Used                   |
|----------------|-----------------------------|------------------------------|
| Amazon Linux   | Base OS + SSH + Updates     | yum, MobaXterm               |
| Ubuntu         | Pentest practice            | Hydra, Nmap                  |
| Windows        | Visual tools + learning     | Wireshark, Nmap GUI          |

---

## ⚠️ Reminder

If you're using the **AWS Free Tier**, be sure to:
- Stop unused instances
- Monitor your billing dashboard
- Set up budget alerts

## 🔧 Scripts

We’ve included setup scripts to help replicate this lab environment faster.

- `scripts/setup-linux.sh`: Updates packages and installs Apache, Hydra, Nmap (Amazon Linux or Ubuntu)
- `scripts/setup-windows.ps1`: Installs Wireshark and Nmap via PowerShell/Chocolatey

To use:

```bash
chmod +x scripts/setup-linux.sh
./scripts/setup-linux.sh

