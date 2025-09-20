# DNS_SPOOFING_6
# DNS_SPOOFING_6 — Safe Isolated Lab

**Author:** Vaishnavi Nagargoje  
**Date:** 2025-09-20

---

## About
This repository documents a safe, offline DNS spoofing lab performed in a VirtualBox Host-Only network. All experiments were executed on local VMs and did **not** touch the public Internet.

> **Important:** This repository is for educational purposes only. Do not run these techniques on public or production networks.

---

## Lab topology (summary)
- Host-only network: `vboxnet0` (`192.168.56.0/24`)  
- Attacker (Kali): `192.168.56.100`  
- Victim (Windows): `192.168.56.118`  
- Server (Ubuntu/Apache): `192.168.56.102`  
(See the report for a full diagram and exact steps.)

---

## Evidence (screenshots)

### 1) Overall lab screenshot
![Lab Overview](DNS_SPOOFING_.png)  
*Figure 1 — Lab overview / high-level screenshot.*

### 2) Ettercap / config edits
![Edit Ettercap conf](edit_ettercap.conf_file.png)  
*Figure 2 — Ettercap configuration edit screen.*

![Changes to etter.conf](changes_etter.conf_file.png)  
*Figure 3 — Changes made to `etter.conf` (sanitized).*

![Changes to etter.conf (alt view)](changes_etter.conf_.png)  
*Figure 4 — Another view of `etter.conf` edits.*

### 3) etter.dns / DNS edits
![etter.dns file changes](etter.dnsfile_changes.png)  
*Figure 5 — Edited `etter.dns` file in the lab (sanitized).*

![changes to etter.dns file](changes_etter.dns_file.png)  
*Figure 6 — `etter.dns` entries showing lab-only mappings.*

![Spoofed etter.dns mapping to attacker IP](etter.dns_spoofed_with_attackers_machineip.png)  
*Figure 7 — Spoofed DNS entry pointing lab domain to attacker's IP (lab-only).*

### 4) Victim browser / fake page
![Victim fake page](example.com_fake_page.png)  
*Figure 8 — Victim browser showing the fake lab page (example.lab / example.com simulated locally).*

### 5) Editor / command proof
![Gedit edit command](gedit_file _edit_command.png)  
*Figure 9 — Command/editor used to edit lab files.*

---

## Included files & suggested organization
_Current files are currently in repo root. Suggested long-term layout (optional):_

