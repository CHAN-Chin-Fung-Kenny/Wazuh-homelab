# Wazuh-homelab
Wazuh-based SOC homelab with Windows, Ubuntu, and Kali attacker

## Lab Architecture
- Wazuh server VM (SIEM/XDR)
- Windows 11 victim (CHINFUNGCHAFEEE)
- Ubuntu 24.04 victim (wazuh agent)
- Kali Linux attacker

## Scenario 1: SSH Brute Force
- Kali uses Hydra to brute force SSH against Ubuntu.
- Wazuh agent on Ubuntu sends auth logs to Wazuh server.
- Wazuh detects repeated SSH failures (rule 5710) and brute-force patterns.

## Skills Demonstrated
- Homelab design and virtualization
- Wazuh installation and agent deployment
- Linux service and networking troubleshooting
- Attack simulation and alert investigation in Wazuh

Add initial homelab README
