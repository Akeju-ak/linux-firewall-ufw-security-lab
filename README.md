# linux-firewall-ufw-security-lab
Linux firewall lab using UFW on Ubuntu, tested with Kali Linux and Nmap

## 📌 Overview
This project demonstrates how to configure a firewall using UFW on Ubuntu and test it using Kali Linux.

## 🎯 Objectives
- Configure firewall rules
- Allow HTTP/HTTPS
- Block SSH access
- Test with Nmap

## 🧪 Lab Setup
- Kali Linux (Attacker)
- Ubuntu (Target)
- Tools: UFW, Nmap, SSH

## ⚙️ Configuration

### Reset Firewall
sudo ufw reset

### Default Rules
sudo ufw default deny incoming
sudo ufw default allow outgoing

### Allow Services
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw allow 22/tcp

### Enable Firewall
sudo ufw enable

## 🔍 Testing

### Before Blocking SSH
nmap <target_ip>

### Block SSH
sudo ufw deny 22/tcp

### After Blocking SSH
nmap <target_ip>

## 🚨 Findings
- Firewall successfully restricted access
- SSH blocked after rule update
- Only necessary ports remained open

## 📸 Screenshots

![UFW Status](screenshots/ufw-status.png)
![Nmap Before](screenshots/nmap-before.png)
![Nmap After](screenshots/nmap-after.png)

## 📄 Report
See full report: report/byteguardian-firewall-project.pdf

## 👤 Author
Emmanuel Akeju
