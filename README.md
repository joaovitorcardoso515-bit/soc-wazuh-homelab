# 🛡️ SOC Wazuh Homelab

A Security Operations Center (SOC) Homelab built with Wazuh to simulate real-world detection, monitoring and incident investigation scenarios.

This project demonstrates the deployment of a SIEM environment capable of monitoring Linux systems, detecting suspicious activities, investigating security events and documenting incident response procedures.

---

# 📌 Project Goals

- Deploy a complete Wazuh environment
- Monitor Linux security events
- Detect privilege escalation
- Detect user creation and account modifications
- Implement File Integrity Monitoring (FIM)
- Simulate attacks from Kali Linux
- Investigate alerts using MITRE ATT&CK
- Build a professional Blue Team portfolio

---

# 🏗️ Architecture

```
                 Windows 11 Host
               (Web Browser)
                      │
                HTTPS (5601)
                      │
                      ▼
        ┌─────────────────────────────┐
        │      Ubuntu Server          │
        │─────────────────────────────│
        │ • Wazuh Dashboard           │
        │ • Wazuh Manager             │
        │ • Wazuh Indexer             │
        │ • Local Agent               │
        └─────────────────────────────┘
                      ▲
                      │
            SSH / Nmap / Attacks
                      │
                Kali Linux
```

---

# 🖥️ Lab Environment

| Component | Description |
|------------|-------------|
| Host OS | Windows 11 |
| Hypervisor | VirtualBox |
| SIEM | Wazuh 4.12 |
| Server | Ubuntu Server 24.04 LTS |
| Attacker Machine | Kali Linux |
| Network | Host-Only + NAT |

---

# 🛠️ Technologies

- Wazuh
- Ubuntu Server
- Kali Linux
- Linux
- VirtualBox
- Syscheck (File Integrity Monitoring)
- Linux Audit
- MITRE ATT&CK
- OpenSearch Dashboard
- Git
- GitHub

---

# 📂 Repository Structure

```
SOC-Wazuh-Homelab/

│
├── README.md
│
├── docs/
│   ├── 01-installation.md
│   ├── 02-user-monitoring.md
│   ├── 03-file-integrity-monitoring.md
│
├── screenshots/
│   ├── dashboard-overview.png
│   ├── user-created-alert.png
│   ├── sudo-alert.png
│   ├── fim-alert.png
│
└── reports/
```

---

# ✅ Completed Scenarios

| Status | Scenario |
|---------|----------|
| ✅ | Ubuntu Server installation |
| ✅ | Wazuh deployment |
| ✅ | Dashboard configuration |
| ✅ | Agent registration |
| ✅ | Linux user creation detection |
| ✅ | Privilege escalation detection (`sudo`) |
| 🚧 | File Integrity Monitoring |
| ⏳ | Nmap Scan Detection |
| ⏳ | SSH Brute Force Detection |
| ⏳ | Active Response |
| ⏳ | Custom Detection Rules |
| ⏳ | Sysmon Integration |

---

# 🔍 Detection Scenarios

## User Creation Detection

A new Linux user was created.

```
sudo adduser socuser
```

Detected by Wazuh:

- New user created
- New group created
- Account modified

---

## Privilege Escalation

Administrative privileges were obtained using:

```
sudo su
```

Detected by Wazuh:

- sudo execution
- Privilege escalation
- Authentication logs

---

## File Integrity Monitoring (In Progress)

The File Integrity Monitoring module is configured to monitor changes in critical Linux directories.

Monitored directories include:

- /etc
- /usr
- /bin

---

# 📸 Screenshots

Example screenshots included in this repository:

- Wazuh Dashboard
- Security Alerts
- User Creation Detection
- Privilege Escalation
- File Integrity Monitoring

---

# 🛡️ MITRE ATT&CK

Examples of techniques observed during the lab:

| Technique | Description |
|------------|-------------|
| T1136 | Create Account |
| T1098 | Account Manipulation |

---

# 📚 Skills Demonstrated

- Security Monitoring
- SIEM Administration
- Linux Administration
- Log Analysis
- Blue Team Operations
- Incident Investigation
- MITRE ATT&CK Mapping
- Security Documentation
- File Integrity Monitoring

---

# 🚀 Future Improvements

- Windows Agent
- Sysmon
- Suricata
- TheHive
- Shuffle SOAR
- Active Response Automation
- Custom Wazuh Rules
- Sigma Rules
- Docker Monitoring
- AWS Cloud Monitoring

---

# 👨‍💻 Author

**João Vitor Cardoso**

Information Security Student

Backend Developer

Blue Team | SOC Analyst

GitHub:

https://github.com/joaovitorcardoso515-bit

LinkedIn:

(Add your LinkedIn profile)

---

⭐ If you found this project useful, feel free to leave a star.