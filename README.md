# Wazuh-SIEM-Defensive-Security
Implementation of Wazuh SIEM for real-time log monitoring and threat detection on Ubuntu and Windows 11
# Defensive Security using Wazuh SIEM

## 📌 Project Overview

This project demonstrates the implementation of a Security Information and Event Management (SIEM) solution using Wazuh in a virtual lab environment.

The system was designed to monitor logs, detect threats, analyze security events, and provide real-time visibility into endpoint activities using Wazuh SIEM.

---

## 🎯 Objectives

* Understand the role of SIEM in defensive security
* Install and configure Wazuh SIEM
* Monitor authentication, system, and application logs
* Detect brute-force and privilege escalation activities
* Implement File Integrity Monitoring (FIM)
* Analyze alerts using MITRE ATT&CK mapping

---

## 🛠 Technologies & Tools

* Wazuh SIEM v4.7.5
* Ubuntu 22.04 LTS
* Windows 11
* Oracle VirtualBox
* PowerShell
* OpenSearch Dashboard

---

## 🖥 Lab Environment

### Wazuh Server

* OS: Ubuntu 22.04 LTS
* IP Address: 192.168.8.155
* RAM: 4GB
* Storage: 25GB
* Hypervisor: Oracle VirtualBox

### Wazuh Agent

* OS: Windows 11
* Agent Name: MyPcWazuhagent
* Wazuh Agent Version: v4.7.5

---

## ⚙ Installation Steps

### Install Wazuh Server

```bash
sudo apt update && sudo apt install curl -y

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh

sudo bash wazuh-install.sh -a
```

### Install Wazuh Agent (Windows PowerShell)

```powershell
Invoke-WebRequest -Uri wazuh-agent-4.7.5-1.msi

msiexec /q WAZUH_MANAGER='192.168.8.155'

NET START WazuhSvc
```

---

## 🔍 Features Implemented

* Real-time log monitoring
* Authentication log analysis
* File Integrity Monitoring (FIM)
* Brute-force attack detection
* Privilege escalation detection
* MITRE ATT&CK mapping
* Dashboard-based security visualization

---

## 🚨 Simulated Attack Scenarios

### 1. Brute-force Login Attempts

Detected multiple failed login attempts using Rule ID 60122.

### 2. Privilege Escalation

Detected elevated privilege access events using Rules 60106 and 60118.

### 3. File Integrity Monitoring (FIM)

Monitored unauthorized file additions, modifications, and deletions in real time.


## 📚 Learning Outcomes

This project improved our practical knowledge in:

* SIEM implementation
* Defensive security
* Threat detection
* Log analysis
* Windows & Linux administration
* Security monitoring and troubleshooting


  

