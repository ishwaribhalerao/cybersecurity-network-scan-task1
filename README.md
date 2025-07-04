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
```
📎 _Screenshot: `02-nmap-scan.jpg`_

### 🔍 Scan Results Summary

| Host IP         | Open Port | Service      | Notes                            |
|-----------------|-----------|--------------|----------------------------------|
| 192.168.38.1    | 7070      | realserver   | Could be a web or proxy server   |
| 192.168.38.2    | 53        | domain (DNS) | Standard DNS service             |
| 192.168.38.254  | None      | All filtered | No response to probes            |
| 192.168.38.128  | None      | All closed   | Host is well-secured             |

---

## 🧪 Wireshark Packet Analysis

- Captured **DNS** and **TLS** traffic.
- Applied filter:  
  ```udp.port == 53```
- Observed secure communication (TLS 1.3) and DNS queries.

📎 _Screenshot: `03-wireshark.jpg`_

---

## 🛡️ Security Analysis

- **Port 7070** is non-standard; investigate its use. It may pose a risk if unnecessary or outdated.
- **Port 53** is expected for DNS but should be monitored for unusual activity (e.g., DNS tunneling).
- **192.168.38.128** (host machine) and **.254** show a strong security posture with no open or responding ports.

---

## ✅ Conclusion

This task helped me understand:

- How to perform a **stealth network scan** using Nmap  
- How to **interpret port and service data** from scan results  
- How to **capture and filter traffic** using Wireshark  
- How to **identify and assess vulnerabilities** in a local network



