## 👤 About Me

I'm Abraham, currently completing my SOC Analyst certification and building this lab to translate theory into hands-on capability. My focus areas: detection engineering, threat hunting, and incident response.

- 
- **Contact:** abrahamabez@gmail.com

---

⭐ *This is a living project — updated weekly as the lab evolves.*

# 🛡️ SOC Home Lab

> A fully functional Security Operations Center built from scratch — designed to develop hands-on SOC analyst skills through realistic detection engineering and incident response scenarios.

[![Status](https://img.shields.io/badge/status-in%20progress-yellow)]()
[![Week](https://img.shields.io/badge/week-1%2F12-blue)]()
[![License](https://img.shields.io/badge/license-MIT-green)]()

## 🎯 Project Goals

- Build a production-grade SOC environment using industry-standard tools
- Generate, detect, and investigate realistic attack scenarios
- Develop detection engineering skills aligned with MITRE ATT&CK
- Practice incident response from detection to reporting
- Document everything as a portfolio of hands-on capabilities

## 🏗️ Architecture

See [docs/01-architecture.md](docs/01-architecture.md) for the full diagram.

**High-level overview:**

- **SOC Node** (i7-1260P, 64GB RAM, Windows 11 + VMware Workstation Pro)
  - Splunk Enterprise (SIEM)
  - Security Onion (NSM — Zeek + Suricata)
  - TheHive + Cortex (Case management)
  - MISP (Threat intelligence)
  - pfSense (Virtual firewall)

- **Target Environment** (Ryzen 3 3200U, 32GB RAM, Windows + VirtualBox)
  - Windows 10 Pro (endpoint with Sysmon)
  - Windows Server 2019 (Active Directory)
  - Ubuntu Server (vulnerable web server)
  - Kali Linux (red team simulator)

## 🛠️ Tech Stack

| Category | Tool |
|----------|------|
| SIEM | Splunk Enterprise |
| NSM | Security Onion (Zeek + Suricata) |
| Endpoint Telemetry | Sysmon + Windows Event Logs + auditd |
| Case Management | TheHive + Cortex |
| Threat Intelligence | MISP |
| Detection Engineering | Sigma rules → SPL |
| Adversary Emulation | Atomic Red Team, Caldera |
| Virtualization | VMware Workstation Pro, VirtualBox |

## 📅 Roadmap

- [x] **Week 1:** Foundation, GitHub setup, hypervisor installation
- [ ] **Week 2:** Base VMs (Ubuntu, Windows 10, Windows Server, Kali)
- [ ] **Week 3-4:** Splunk Enterprise deployment & Universal Forwarders
- [ ] **Week 5-6:** Endpoint visibility — Sysmon, auditd, custom dashboards
- [ ] **Week 7-8:** Detection engineering — Sigma rules, alerts, threat hunting
- [ ] **Week 9-10:** Network Security Monitoring — Security Onion, PCAP analysis
- [ ] **Week 11-12:** Full incident response simulation

## 📖 Lessons Learned

Weekly notes documenting challenges, decisions, and key takeaways:
[docs/03-lessons-learned.md](docs/03-lessons-learned.md)

## 📂 Repository Structure
soc-home-lab/
├── docs/             → Architecture, setup guides, lessons learned
├── configs/          → Configuration files (Sysmon, Splunk, etc.)
├── detections/       → Sigma rules and SPL queries
├── playbooks/        → Incident response procedures
├── incidents/        → Writeups of simulated incidents
└── screenshots/      → Dashboard captures and evidence
