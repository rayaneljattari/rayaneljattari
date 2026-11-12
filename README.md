<div align="center">

<img src="assets/banner.svg" alt="Rayan El Jattari · Cybersecurity student" width="100%">

<h1>👋 Hey, I'm Rayan El Jattari</h1>

<b>Cybersecurity Student · Aspiring Security Consultant · Homelab Builder</b>

I build small company networks at home, harden them, attack them, and write up what I find as if a client were reading it.

<br>

<a href="https://www.linkedin.com/in/rayan-el-jattari-41a6353a2"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="https://github.com/rayaneljattari/enterprise-security-homelab"><img src="https://img.shields.io/badge/Homelab-161b22?style=for-the-badge&logo=github&logoColor=white" alt="Homelab"></a>
<img src="https://img.shields.io/badge/Antwerp%2C_Belgium-1f6feb?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Antwerp, Belgium">
<img src="https://img.shields.io/badge/Open_to-internships-2ea043?style=for-the-badge&logo=handshake&logoColor=white" alt="Open to internships">

<br><br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=17&duration=3500&pause=1200&color=3FB8FF&center=true&vCenter=true&width=560&lines=Harden+it.+Attack+it.+Detect+it.+Document+it.;Active+Directory+%C2%B7+Wazuh+SIEM+%C2%B7+Kali+%C2%B7+Raspberry+Pi;Looking+for+a+junior+role+in+security+consulting" alt="Harden it. Attack it. Detect it. Document it.">

<br>

**Jump to:** 🧭 [At a glance](#-at-a-glance) · 🛡️ [Projects](#%EF%B8%8F-projects) · 🧪 [Home lab](#-home-lab-stack) · 🧰 [Toolbox](#-toolbox) · 🗺️ [Roadmap](#%EF%B8%8F-roadmap)

</div>

---

## 🧭 At a glance

| | |
|---|---|
| 🎓 **Education** | Bachelor in Cybersecurity at AP Hogeschool Antwerp, 2nd year |
| 🎯 **Goal** | Junior cybersecurity consultant in Belgium: helping organisations understand their risks and fix them |
| 🏢 **Lab scenario** | Scheldt Logistics NV, a fictional 60-person company in Antwerp that falls under NIS2 |
| 💻 **Hardware** | MacBook Pro M4 Pro running ARM64 VMs in UTM, plus a Raspberry Pi for edge services |
| 🔍 **Focus** | Identity security (Active Directory), hardening, detection with a SIEM, and clear reporting |
| 🗣️ **Languages** | Dutch · English · French · Arabic |

I'm most interested in where security meets the business: working out what an organisation actually needs to protect, finding where it's weak, and turning that into advice people can act on. Every project here is written up with that in mind.

---

## 🛡️ Projects

| Project | What it does | Status |
|---|---|---|
| [**enterprise-security-homelab**](https://github.com/rayaneljattari/enterprise-security-homelab) | Full small-company network: Active Directory with admin tiering and hardening, Wazuh SIEM, attack simulation from Kali, hardened Raspberry Pi. Delivered like a client engagement with scripts, configs, a test plan and business impact. | 🟡 Build in progress |

```mermaid
flowchart LR
    KALI["KALI01<br/>attack simulation"] -->|password spray| DC
    subgraph LAB["Scheldt Logistics · 10.10.10.0/24"]
        GW["GW01<br/>nftables router"]
        DC["DC01<br/>AD · DNS · GPO"]
        CL["CL01<br/>workstation"]
        SIEM["SIEM01<br/>Wazuh"]
    end
    GW --- DC
    CL --- DC
    DC -. logs .-> SIEM
    CL -. logs .-> SIEM
    PI["pi01<br/>Pi-hole · WireGuard"] --- GW
```

<sub>More projects will be added here as I build them.</sub>

---

## 🧪 Home lab stack

### 🏢 Identity
- Windows Server 2025 domain controller with DNS and Group Policy
- Department OU structure, 60 users provisioned with PowerShell
- Admin tiering, Windows LAPS, Protected Users

### 🔒 Hardening
- 14-character password policy with lockout, no forced expiry
- LLMNR and Print Spooler disabled on the DC, advanced audit policy
- Before/after measurement with PingCastle

### 📡 Detection
- Wazuh SIEM on Ubuntu with agents on the DC and workstation
- Authorised attack simulation from Kali to test what gets detected

### 🌐 Network & edge
- Debian router with nftables and NAT
- Raspberry Pi with Pi-hole, WireGuard and Uptime Kuma in Docker, hardened with ufw, fail2ban and key-only SSH

---

## 🧰 Toolbox

<p>
  <img src="https://img.shields.io/badge/Windows_Server-0078D4?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Server">
  <img src="https://img.shields.io/badge/Active_Directory-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" alt="Active Directory">
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white" alt="PowerShell">
  <img src="https://img.shields.io/badge/Wazuh-3595F9?style=for-the-badge&logo=wazuh&logoColor=white" alt="Wazuh">
  <img src="https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white" alt="Kali Linux">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
  <img src="https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white" alt="Bash">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberrypi&logoColor=white" alt="Raspberry Pi">
  <img src="https://img.shields.io/badge/WireGuard-88171A?style=for-the-badge&logo=wireguard&logoColor=white" alt="WireGuard">
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
</p>

---

## 🗺️ Roadmap

- [ ] Finish the homelab build and publish screenshots and results
- [ ] Before/after AD security score with PingCastle
- [ ] Entra ID hybrid identity with MFA and Conditional Access
- [ ] NIS2 / CyFun gap assessment report for the fictional client
- [ ] Network segmentation between attacker, server and client networks

---

<div align="center">

### 🤝 Let's connect

I'm looking for internships and student jobs in cybersecurity in Belgium.<br>
The best way to reach me is on [**LinkedIn**](https://www.linkedin.com/in/rayan-el-jattari-41a6353a2).

<br>

<sub>🛡️ Blue team · 🏢 Active Directory · 📡 SIEM · 🐧 Linux · 🍓 Raspberry Pi · 🇧🇪 Antwerp</sub>

</div>
