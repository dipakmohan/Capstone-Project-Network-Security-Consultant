# 🛡️ Network Security Consultant – Capstone Project

**Advanced Executive Program in Cybersecurity  
Virtual Internship Project – IIIT Bangalore**

## 👨‍💻 Submitted By:
**Deepak Sharma**

---

## 📘 Project Overview

This project simulates the responsibilities of a **Network Security Consultant** at a fictional financial institution — **El Banco Bank** — which manages €200 billion in assets and operates over 1200 branches across Europe.

As a consultant, the key objective is to **secure critical digital infrastructure** by reviewing digital certificate issues, hardening firewall rules, configuring VPNs for remote access, and ensuring secure file transfer practices.

---

## 🧾 Tasks Covered

### ✅ **Task 1 – Digital Certificate Issue Troubleshooting**
Resolved common certificate-related support tickets:

| Ticket # | Issue Description                               | Resolution Summary                                      |
|----------|--------------------------------------------------|---------------------------------------------------------|
| 1        | Browser shows SSL error when using IP address    | Certificates are issued for domains, not IPs. Use FQDN. |
| 2        | Certificate shows expired despite renewal        | Cached cert or clock error. Restart server and resync.  |
| 3        | Root certificate not trusted                     | Root CA missing on client. Install or update trust store. |

---

### ✅ **Task 2 – Firewall Rule Configuration**

Configured **inbound firewall rules** for a cloud-hosted VM, allowing access only to authorized services and IPs:

| Type        | Protocol | Port | Source          |
|-------------|----------|------|------------------|
| HTTPS       | TCP      | 443  | 0.0.0.0/0        |
| RDP Service | TCP      | 3389 | 18.66.78.112/32  |
| SSH Service | TCP      | 22   | 18.66.78.112/32  |

---

### ✅ **Task 3 – VPN Access Design**

Designed **two VPN configurations** for secure remote access:

| OS      | VPN Type     | Protocol | Tunnel Method | Port | Notes                                                             |
|---------|--------------|----------|----------------|------|-------------------------------------------------------------------|
| Ubuntu  | Host-to-site | OpenVPN  | Full Tunnel    | 1194 | Secure SSL/TLS VPN. All traffic routed through corporate network |
| Windows | Host-to-site | PPTP     | Split Tunnel   | 1723 | Lightweight access. Allows Netflix bypass via local ISP          |

> Both VPNs support **256-bit encryption** and use **SSL/TLS key exchange**.

---

### ✅ **Task 4 – Secure File Transfer with Certificate Verification**

- Configured secure file transfer using **SFTP over SSH (port 22)**
- Verified the VM’s digital certificate using:
  - `openssl s_client -connect domain:443`
  - `ssh-keygen -lf ssh_host_key.pub`
- Hardened firewall to only allow file transfers from trusted sources

---

## 🔐 Key Security Practices Applied

- Principle of **least privilege** in firewall access
- **Zero trust** remote access with VPN
- Use of **strong encryption (TLS, 256-bit)**
- Ensured **digital certificate integrity and validity**
- Performed **client-side and server-side certificate troubleshooting**

---


---

## 📌 Tools Used

- `openssl`
- PowerShell
- Git Bash / Terminal
- Cloud VM (Linux/Windows)
- SSH/SFTP
- Certificate viewers (Browser/CLI)

---

## 📄 License

This project is part of the **Advanced Executive Program in Cybersecurity** (IIIT Bangalore) and is submitted for educational purposes only.

---



