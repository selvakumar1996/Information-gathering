# 🌐 Information Gathering & Web Enumeration Project

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Tool](https://img.shields.io/badge/Tools-Nmap%2C%20Nikto%2C%20Dirb%2C%20WhatWeb-blue)
![Category](https://img.shields.io/badge/Category-Reconnaissance-red)
![Language](https://img.shields.io/badge/Language-MD-yellow)

## 🎯 Objective
To perform **information gathering and web enumeration** on vulnerable web applications hosted on **OWASP BWA** using tools like:  

- Nikto  
- Nmap  
- Ping  
- Nslookup  
- Host  
- Google Dorks  
- WhatWeb  
- Dirb  

---

## ⚙️ Lab Setup
1. Download and run **OWASP BWA** in VMware/VirtualBox (Bridged Adapter).  
2. Find OWASP BWA IP using `ip a` in terminal.  
3. Ensure **Kali Linux attacker machine** and **OWASP BWA target VM** can ping each other.  

---

## 🚀 Project Steps

### 1️⃣ Ping the Target
```bash
ping <OWASP-BWA-IP>
```

### 2️⃣ DNS Enumeration
```bash
nslookup <OWASP-BWA-IP>
host <OWASP-BWA-IP>
```

### 3️⃣ Nmap Scans
```bash
nmap -sS <OWASP-BWA-IP>          # Basic Scan
nmap -A <OWASP-BWA-IP>           # Aggressive Scan
nmap --script vuln <OWASP-BWA-IP> # Vulnerability Scan
```

### 4️⃣ WhatWeb Scan
```bash
whatweb http://<OWASP-BWA-IP>
```

### 5️⃣ Directory Brute Forcing (Dirb)
```bash
dirb http://<OWASP-BWA-IP>
```

### 6️⃣ Vulnerability Scan (Nikto)
```bash
nikto -h http://<OWASP-BWA-IP>
```

### 7️⃣ Google Dorks (Browser)
Examples:  
```
site:<target>  
inurl:admin  
intitle:"index of"  
filetype:php  
```

---

## 📂 Deliverables
- Screenshots of each command and result.  
- Documented observations (open ports, web technologies, directories, vulnerabilities).  
- Final Report (PDF/DOCX) containing:  
  - Introduction  
  - Methodology  
  - Tools Used  
  - Findings  
  - Conclusion  

---

## 💡 Bonus Tips
- Use `-oN result.txt` in Nmap to save results.  
- Compare findings across tools.  
- Add mitigation steps or charts for professional reporting.  

---

## 📊 Attack Workflow Diagram

```mermaid
flowchart TD
    A[Attacker: Kali Linux] -->|Ping / Nmap / Nikto / Dirb / WhatWeb| B[Target: OWASP BWA]
    B --> C[Open Ports & Services]
    B --> D[Web Directories & Files]
    B --> E[Vulnerabilities Identified]
    E --> F[Report Findings & Mitigation]
```
