# 🧪 Lab Setup Guide – Home Cyber Range SOC Lab

## 📌 Overview

This document describes the setup of a controlled home cyber range environment used to simulate real-world attack and defense scenarios.

The lab is designed with **network isolation** to prevent exposing vulnerable systems to the internet.

---

## 🖥️ Virtual Machines

| Machine        | Role                   |
| -------------- | ---------------------- |
| Kali Linux     | Attacker (Red Team)    |
| Ubuntu Server  | Target system          |
| Metasploitable | Vulnerable target      |
| Wazuh / ELK    | Monitoring & Detection |

---

## 🌐 Network Configuration

To ensure both **functionality and security**, a dual-network approach was used:

* **NAT Adapter** → Internet access (updates, tools)
* **Host-Only Adapter** → Isolated internal lab network

---

## 🔧 Kali Linux Configuration

* Adapter 1: NAT (Internet access)
* Adapter 2: Host-Only Adapter (Lab network)

![Kali Network Settings](screenshots/kali-network.png)

---

## 🔧 Ubuntu Server Configuration

* Adapter 1: NAT (Internet access)
* Adapter 2: Host-Only Adapter (Lab network)

![Ubuntu Network Settings](screenshots/ubuntu-network.png)

---

## 🔧 Metasploitable Configuration

* Adapter 1: Host-Only Adapter ONLY

This ensures:

* The vulnerable system is **fully isolated**
* No exposure to external networks
* Safe exploitation within the lab environment

![Metasploitable Network Settings](screenshots/metasploitable-network.png)

---

## 🧠 Network Design Rationale

This architecture ensures:

### ✅ Isolation of Vulnerable Systems

Metasploitable is not connected to the internet, preventing accidental exposure.

### ✅ Controlled Attack Environment

Kali can attack targets via the host-only network.

### ✅ Internet Access for Tools

Kali and Ubuntu can still install tools and updates via NAT.

---

## 🔍 IP Address Verification

Each machine was verified using:

```bash
ip a
```

All lab machines share the same **host-only network range**, enabling communication.

---

## 🔐 Security Considerations

* Vulnerable machines are isolated from external networks
* No port forwarding enabled
* Firewall rules can be applied using UFW
* Traffic monitoring enabled via Suricata and Wazuh

---

## 🚧 Next Steps

* Deploy vulnerable applications (DVWA / Juice Shop)
* Install and configure Wazuh SIEM
* Integrate ELK stack
* Set up Suricata IDS
* Begin attack simulations

---

## 📚 Notes

This lab forms the foundation for:

* Detection engineering
* Threat hunting
* Incident response simulations
