# 🔐 Cyber Security Task – Nmap Network Scan & Packet Analysis

This repository contains the results of a cybersecurity task where I scanned my local network using **Nmap** and analyzed traffic with **Wireshark** as part of my internship learning activities.

---

## 📌 Task Objectives

- Scan the local network using **Nmap** to identify live hosts and open ports.
- Capture and inspect traffic using **Wireshark**.
- Identify and evaluate potential vulnerabilities based on scan results.

---

## 🧰 Tools Used

- 🖥️ **Kali Linux**
- 🔍 **Nmap** – Network scanning
- 📡 **Wireshark** – Packet capture and protocol analysis
- 📷 Screenshots for documentation

---

## 🛠️ Task Steps & Observations

### 1. Identify IP Range
Used `ifconfig` to find my local IP address and subnet:

- **IP Address**: `192.168.38.128`
- **Network/Subnet**: `192.168.38.0/24`

📎 _Screenshot: `01-ifconfig.jpg`_

---

### 2. Run Nmap SYN Scan

Command used:
```bash
nmap -sS 192.168.38.0/24
