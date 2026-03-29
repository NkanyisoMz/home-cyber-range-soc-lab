# 🛡️ Home Cyber Range SOC Lab

## 📌 Overview

This project simulates a real-world Security Operations Center (SOC) environment where both offensive (Red Team) and defensive (Blue Team) activities are performed.

The lab is designed to demonstrate:

* Attack simulation (Red Team)
* Detection engineering (Blue Team)
* Log analysis and threat hunting
* Incident response workflows

---

## 🧱 Architecture

The lab consists of:

* **Kali Linux** (Attacker machine)
* **Ubuntu Server** (Target system)
* **DVWA / Juice Shop** (Vulnerable applications)
* **Metasploitable** (Intentionally vulnerable VM)
* **Wazuh SIEM**
* **ELK Stack (Elasticsearch, Logstash, Kibana)**
* **Suricata IDS**

---

## 🎯 Objectives

* Simulate real-world cyber attacks
* Detect malicious behavior using SIEM and IDS tools
* Analyze logs and identify Indicators of Compromise (IOCs)
* Build and test detection rules
* Perform incident response and mitigation

---

## ⚙️ Technologies Used

* Wazuh (SIEM)
* ELK Stack
* Suricata
* Docker
* Nmap
* Metasploit
* Wireshark
* UFW Firewall

---

## 🔴 Attack Scenarios

| Scenario             | Description                  |
| -------------------- | ---------------------------- |
| Brute Force          | SSH login attack using Hydra |
| Reverse Shell        | Gaining remote shell access  |
| Privilege Escalation | Escalating user privileges   |

---

## 🔵 Detection Engineering

Custom detection rules are created using:

* Wazuh rules
* Suricata signatures

---

## 🔍 Log Analysis

Logs are analyzed using Kibana dashboards and Wazuh alerts to:

* Identify anomalies
* Correlate events
* Investigate incidents

---

## 🛡️ Incident Response

Each attack scenario includes:

* Detection
* Analysis
* Mitigation strategies

---

## 📚 Lessons Learned

Documented in [lessons-learned.md](lessons-learned.md)

---

## 🚧 Future Improvements

* Add automated alerting
* Integrate threat intelligence feeds
* Expand attack scenarios
