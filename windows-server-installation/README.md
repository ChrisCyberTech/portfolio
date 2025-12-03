# 🖥️ Windows Server Installation & Domain Controller Setup

This lab demonstrates the complete process of building a **Windows Server 2025 virtual machine**, configuring core server roles, and promoting it to a **Domain Controller (DC01)**.  
It serves as a foundational step in enterprise network management and prepares the environment for Active Directory user, group, and policy management.

---

## 🧩 Overview

This project covers:
- Downloading and configuring a Windows Server VHDX image  
- Importing and setting up the virtual machine in UTM  
- Installing Active Directory Domain Services (AD DS)  
- Promoting the server to a Domain Controller (`DC01`)  
- Verifying domain login with the administrator account  

---

## 🧱 Environment

| Component | Description |
|------------|-------------|
| **Hypervisor** | UTM on macOS |
| **OS Image** | Windows Server 2025 Insider Preview (VHDX) |
| **Domain** | `lab.local` |
| **Hostname** | `DC01` |
| **Role** | Active Directory Domain Controller |
| **Network** | Static IP with DNS set to DC01 |

---

## 🧭 Installation Steps

### 1️⃣ Download and Prepare the Server Image
![L4-S00a–Insider-Server-VHDX-Download-Page](./screenshots/L4-S00a–Insider-Server-VHDX-Download-Page.png)
![L4-S00b–Extracted-VHDX-File](./screenshots/L4-S00b–Extracted-VHDX-File.png)
![L4-S00c–UTM-Import-Settings](./screenshots/L4-S00c–UTM-Import-Settings.png)

---

### 2️⃣ Begin Installation
![Installing-Windows-Server](./screenshots/Installing-Windows-Server.png)
![Windows-Server-Setup-Administrator-Password-Screen](./screenshots/Windows-Server-Setup-Administrator-Password-Screen.png)
![Windows-Server-Installed-and-Booted-to-Server-Manager](./screenshots/Windows-Server-Installed-and-Booted-to-Server-Manager.png)

---

### 3️⃣ Build Server ISO and Configure Networking
![ServerISO-Build-Complete](./screenshots/ServerISO-Build-Complete.png)
![6.1-Rename-Server-to-DC01](./screenshots/6.1-Rename-Server-to-DC01.png)
![6.3-Static-IP-and-DNS-configuration-for-DC01](./screenshots/6.3-Static-IP-and-DNS-configuration-for-DC01.png)

---

### 4️⃣ Install and Configure Active Directory
![6.4-Installing-Active-Directory-Domain-Services-on-DC01](./screenshots/6.4-Installing-Active-Directory-Domain-Services-on-DC01.png)
![Review-Options-before-Domain-Controller-Installation](./screenshots/Review-Options-before-Domain-Controller-Installation.png)
![6.5-AD-DS-installation-complete-ready-for-promotion](./screenshots/6.5-AD-DS-installation-complete-ready-for-promotion.png)

---

### 5️⃣ Verify Domain Controller Login
![6.9-Successful-Domain-Controller-Login-LAB-Administrator](./screenshots/6.9-Successful-Domain-Controller-Login-LAB-Administrator.png)

---

## ✅ Outcome

By the end of this lab:
- The server was successfully renamed to **DC01**
- Networking was configured with static IP and internal DNS
- Active Directory Domain Services were installed and promoted
- Domain controller verified via **LAB\Administrator** login

---


---

## 🧠 Skills Demonstrated

- Windows Server installation and configuration  
- Virtualization setup using UTM  
- Static IP and DNS setup  
- Active Directory Domain Services configuration  
- Domain controller promotion  
- Administrative login validation  

---

## 🪪 Author
**Luis C. Mejia**  
🖥️ [GitHub: ChrisCyberTech](https://github.com/ChrisCyberTech)

---




