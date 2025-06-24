# 🛡️ Wazuh + Suricata Integration for Threat Detection

This project demonstrates the integration of **Wazuh** (HIDS) and **Suricata** (NIDS) in a simulated lab environment to detect and analyze security threats in real-time.

## 📌 Project Objectives

- Implement a SIEM system using Wazuh and Suricata.
- Simulate network attacks and analyze the alerts generated.
- Understand how HIDS and NIDS work together for better threat visibility.

---

## 🖥️ Lab Architecture

```
[ Kali Linux ] → (Simulated Attacks)
         |
[ Ubuntu VM with Suricata + Wazuh Agent ]
         |
[ Wazuh Server ]
```

- **Wazuh Server:** Collects and visualizes alerts.
- **Wazuh Agent + Suricata:** Installed on monitored VM to detect host and network threats.
- **Kali Linux:** Used to simulate attacks (e.g., Nmap scan, malware traffic, brute force).

---

## ⚙️ Tools & Technologies

| Tool         | Function                          |
|--------------|-----------------------------------|
| Wazuh        | Host-based Intrusion Detection    |
| Suricata     | Network Intrusion Detection System|
| Kali Linux   | Attack simulation                 |
| VirtualBox   | VM virtualization                 |

---

## 🚀 Features

- ✅ Real-time alert monitoring via Kibana
- ✅ Detection of malicious traffic (e.g., spyware, trojan, PUP)
- ✅ Integration of Suricata logs into Wazuh alert engine
- ✅ Visualization of Suricata alerts in Wazuh dashboard

---

## 📷 Screenshots

### 🔍 Kibana Discover View
![Kibana Discover](assets/kibana_discover.png)

### 📈 Alert Visualization
![Kibana Alerts](assets/alert_chart.png)

---

## 🧪 Attack Simulation Examples

| Attack Type             | Tool Used     | Detected Alert                           |
|--------------------------|---------------|-------------------------------------------|
| Port Scanning           | Nmap          | Suricata: ET SCAN Nmap Scripting Engine   |
| Malicious Beaconing     | Custom PCAP   | Suricata: ET MALWARE CnC Beacon Detected  |
| Brute-force SSH         | Hydra         | Wazuh: SSH brute force attempt            |

---

## 📚 What I Learned

- How to configure and manage a Wazuh SIEM setup
- Integrating Suricata with Wazuh for comprehensive threat detection
- Analyzing network and host logs effectively
- Realizing the power of HIDS + NIDS combination

---

## 🔧 How to Run (Simplified)

> All components run on separate VirtualBox VMs.

1. Clone this repo
2. Follow installation guides:
   - [Wazuh Installation Guide](https://documentation.wazuh.com/current/installation-guide/)
   - [Suricata Install Docs](https://suricata.io/docs/)
3. Configure `ossec.conf` and Suricata Eve JSON output
4. Start Wazuh agent and Suricata
5. Launch Kibana to view alerts

---

## 📁 Project Structure

```
wazuh-suricata-project/
│
├── config/                   # Configuration files
├── docs/                     # Documentation & diagrams
├── logs/                     # Sample logs (sanitized)
├── assets/                   # Screenshots for README
└── README.md                 # This file
```

---
📚 References
Wazuh Documentation
Suricata Docs
Wazuh + Suricata Integration Guide

## 📬 Contact

**Zaidan Mahfudz Azzam Saidi**  
_Information Technology Student | Cybersecurity Enthusiast_  
📧 [LinkedIn](https://linkedin.com/in/zaidanmahfudz) | 🌐 [GitHub](https://github.com/ZaanmaVerse)
