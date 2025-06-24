# 🔐 SIEM Integration Project: Wazuh + Suricata

This project demonstrates a **Security Information and Event Management (SIEM)** solution using **Wazuh** as the Host-based Intrusion Detection System (HIDS) and **Suricata** as the Network-based Intrusion Detection System (NIDS).

> 🎓 Developed as a student project to explore real-world threat monitoring and detection on a multi-VM lab environment.

---

## 📌 Project Objectives

- Integrate **Wazuh** and **Suricata** for endpoint and network threat detection.
- Simulate real attacks using **Kali Linux** and observe detection in **Wazuh Dashboard**.
- Learn and apply best practices in security monitoring, event correlation, and alerting.

---

## 🧱 Architecture

+----------------+ Internal Network +------------------+
| Kali Linux | <-----------------------> | Ubuntu (Agent + |
| (Attacker VM) | | Suricata Sensor)|
+----------------+ +------------------+
|
| Agent
v
+------------------+
| Wazuh Server |
| (Ubuntu Server) |
+------------------+

yaml
Salin
Edit

- **VM1**: Wazuh Server + Dashboard  
- **VM2**: Wazuh Agent (target machine)  
- **VM3**: Wazuh Agent + Suricata (NIDS sensor)  
- **VM4**: Kali Linux (attack simulator)

---

## 🚀 Features

- ✅ Wazuh Agent and Server communication setup
- ✅ Suricata rules & signatures for network-based detection
- ✅ Integration logs forwarded to Wazuh Manager
- ✅ Custom alert rules and monitoring via dashboard
- ✅ Simulated attacks: Nmap, brute-force, and reverse shell

---

## ⚙️ How to Deploy

### 1. Clone this repository
```bash
git clone https://github.com/yourusername/wazuh-suricata-project.git
cd wazuh-suricata-project
2. Configure Wazuh Agents
Install agent on VM2 and VM3

Register with Wazuh Manager using:

bash
Salin
Edit
/var/ossec/bin/agent-auth -m <WAZUH_SERVER_IP>
3. Install & Configure Suricata on VM3
bash
Salin
Edit
sudo apt update && sudo apt install suricata
sudo suricata -c /etc/suricata/suricata.yaml -i eth1
4. Forward Suricata Logs to Wazuh Agent
Edit ossec.conf on VM3 agent:

xml
Salin
Edit
<localfile>
  <log_format>json</log_format>
  <location>/var/log/suricata/eve.json</location>
</localfile>
5. Access Wazuh Dashboard
Open your browser:

cpp
Salin
Edit
https://<WAZUH_SERVER_IP>
📁 Project Structure
pgsql
Salin
Edit
├── wazuh-suricata-project/
│   ├── docs/
│   │   └── architecture.png
│   ├── configs/
│   │   ├── suricata.yaml
│   │   └── ossec.conf
│   ├── rules/
│   │   └── local_rules.xml
│   ├── screenshots/
│   │   └── attack-detected.png
│   └── README.md
📸 Screenshots
Simulated Attack	Wazuh Alert

📚 References
Wazuh Documentation

Suricata Docs

Wazuh + Suricata Integration Guide

🧑‍💻 Author
Zaidan Mahfudz Azzam
Information Technology Student | Cybersecurity Enthusiast

📫 Reach me on LinkedIn or via Email
