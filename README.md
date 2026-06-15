# Wazuh-homelab
A Wazuh-based SOC homelab built to practice SIEM monitoring, endpoint visibility, attack simulation, and alert investigation using Windows, Ubuntu, and Kali Linux virtual machines.

## Overview
This project simulates a small blue-team lab environment using Wazuh as the central SIEM/XDR platform. The goal is to build hands-on experience with endpoint monitoring, attack detection, and security investigation workflows.

## Lab Architecture
- Wazuh server VM (SIEM/XDR)
- Windows 11 victim (CHINFUNGCHAFEEE)
- Ubuntu 24.04 victim (wazuh agent)
- Kali Linux attacker

## Scenario 1: SSH Brute Force
- Kali uses Hydra to brute force SSH against Ubuntu.
- Wazuh agent on Ubuntu sends auth logs to Wazuh server.
- Wazuh detects repeated SSH failures (rule 5710) and brute-force patterns.

### Attack Flow
- SSH was enabled on the Ubuntu victim.
- A test user account was created on the Ubuntu VM.
- The Kali attacker used Hydra with a password list to generate repeated failed SSH login attempts.
- The Ubuntu Wazuh agent forwarded authentication logs to the Wazuh server.
- Wazuh detected the failed login activity and generated SSH-related alerts in Threat Hunting.

### Detection Results
- Repeated SSH authentication failures were detected.
- Wazuh generated alert rule `5710` for failed login attempts.
- The lab successfully demonstrated end-to-end detection from attacker activity to SIEM alert visibility.

## Skills Demonstrated
- Homelab design and virtualization
- Wazuh server installation and agent deployment
- Linux service and networking troubleshooting
- SSH attack simulation with Kali Linux and Hydra
- SIEM investigation using Wazuh Threat Hunting
- Log analysis and alert validation

## Screenshots
Add screenshots here showing:

1. Wazuh agent overview
2. Ubuntu Wazuh agent running
3. Hydra brute-force attack from Kali
4. Wazuh Threat Hunting detection results

Add initial homelab README
