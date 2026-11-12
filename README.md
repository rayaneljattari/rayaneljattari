<div align="center">

<h1>Hey, I'm Rayan 👋</h1>

<b>Cybersecurity student · future security consultant · homelab builder</b><br>
<sub>Antwerp, Belgium</sub>

<br><br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=18&duration=3500&pause=1200&color=58A6FF&center=true&vCenter=true&width=520&lines=Harden+it.+Attack+it.+Detect+it.+Document+it.;Active+Directory+%C2%B7+Wazuh+SIEM+%C2%B7+Kali+%C2%B7+Raspberry+Pi;Looking+for+a+junior+role+in+security+consulting" alt="Harden it. Attack it. Detect it. Document it.">

<br>

<a href="https://www.linkedin.com/in/rayan-el-jattari-41a6353a2"><img src="https://img.shields.io/badge/LinkedIn-Rayan_El_Jattari-0d1117?style=for-the-badge&logo=linkedin&logoColor=0A66C2&labelColor=161b22" alt="LinkedIn"></a>
<a href="https://github.com/rayaneljattari/enterprise-security-homelab"><img src="https://img.shields.io/badge/Homelab-enterprise--security--homelab-0d1117?style=for-the-badge&logo=github&logoColor=white&labelColor=161b22" alt="Homelab repo"></a>
<img src="https://img.shields.io/badge/Open_to-internships_%26_junior_roles-0d1117?style=for-the-badge&logo=hackthebox&logoColor=9fef00&labelColor=161b22" alt="Open to internships and junior roles">

</div>

---

## 🧭 At a glance

| | |
|---|---|
| 🎓 **Studying** | Bachelor in Cybersecurity at AP Hogeschool Antwerp, 2nd year |
| 🎯 **Aiming for** | Junior cybersecurity consultant in Belgium |
| 🧪 **Building** | An enterprise-style security homelab for a fictional NIS2 company |
| 💻 **Lab hardware** | MacBook Pro M4 Pro (UTM, all ARM64) + a Raspberry Pi |
| 🗣️ **Languages** | Dutch · English · French · Arabic |
| 🧠 **Interested in** | Identity security, detection, hardening, and turning findings into advice a business can act on |

I like the part where security meets the business: working out what a company actually needs to
protect, finding where it's weak, and explaining the fix so people can act on it. My lab is built
the same way: a fictional client, real configs, a test plan, and a write-up as if I were handing
it over.

---

## 🛡️ Featured project

### [enterprise-security-homelab](https://github.com/rayaneljattari/enterprise-security-homelab) <sub>· build in progress</sub>

A full small-company network for **Scheldt Logistics NV**, a fictional 60-person logistics firm in
Antwerp that falls under NIS2. I design it, harden it, attack it and check what the SIEM catches.

```mermaid
flowchart LR
    KALI["🐉 KALI01<br/>attack simulation"] -->|password spray| DC
    subgraph LAB["Lab network 10.10.10.0/24"]
        GW["🧱 GW01<br/>nftables router"]
        DC["🏢 DC01<br/>Active Directory · DNS · GPO"]
        CL["💻 CL01<br/>domain workstation"]
        SIEM["📡 SIEM01<br/>Wazuh"]
    end
    CL --- DC
    DC -. logs .-> SIEM
    CL -. logs .-> SIEM
    GW --- DC
    PI["🍓 pi01<br/>Pi-hole · WireGuard · Uptime Kuma"] --- GW
```

| Area | What I'm doing |
|---|---|
| **Identity** | AD with department OUs, 60 users provisioned in PowerShell, admin tiering, Windows LAPS, Protected Users |
| **Hardening** | 14-char password policy with lockout, LLMNR and Print Spooler off on the DC, advanced audit policy, before/after check with PingCastle |
| **Detection** | Wazuh agents on the DC and workstation; password spray from Kali should show up as failed-logon alerts |
| **Edge** | nftables router/NAT; Raspberry Pi hardened with ufw, fail2ban, key-only SSH, Docker services |
| **Business side** | Written up for the client: decisions, test plan, and how it maps to NIS2 / CyFun gaps |

<sub>Next up: Entra ID hybrid identity with MFA, a NIS2 / CyFun gap assessment, and network segmentation.</sub>

---

## 🧰 Stack I'm working with

<p>
  <img src="https://img.shields.io/badge/Windows_Server-161b22?style=for-the-badge&logo=windows&logoColor=white" alt="Windows Server">
  <img src="https://img.shields.io/badge/Active_Directory-161b22?style=for-the-badge&logo=microsoft&logoColor=white" alt="Active Directory">
  <img src="https://img.shields.io/badge/PowerShell-161b22?style=for-the-badge&logo=powershell&logoColor=5391FE" alt="PowerShell">
  <img src="https://img.shields.io/badge/Wazuh-161b22?style=for-the-badge&logo=wazuh&logoColor=3595F9" alt="Wazuh">
  <img src="https://img.shields.io/badge/Kali_Linux-161b22?style=for-the-badge&logo=kalilinux&logoColor=557C94" alt="Kali Linux">
  <br>
  <img src="https://img.shields.io/badge/Linux-161b22?style=for-the-badge&logo=linux&logoColor=FCC624" alt="Linux">
  <img src="https://img.shields.io/badge/Bash-161b22?style=for-the-badge&logo=gnubash&logoColor=4EAA25" alt="Bash">
  <img src="https://img.shields.io/badge/Docker-161b22?style=for-the-badge&logo=docker&logoColor=2496ED" alt="Docker">
  <img src="https://img.shields.io/badge/Raspberry_Pi-161b22?style=for-the-badge&logo=raspberrypi&logoColor=A22846" alt="Raspberry Pi">
  <img src="https://img.shields.io/badge/WireGuard-161b22?style=for-the-badge&logo=wireguard&logoColor=88171A" alt="WireGuard">
  <img src="https://img.shields.io/badge/Git-161b22?style=for-the-badge&logo=git&logoColor=F05032" alt="Git">
</p>

---

## 📈 Right now

- 🔨 Building the homelab and documenting every step, screenshots included
- 📚 Second year of my cybersecurity bachelor
- 🤝 Open to internships and student jobs in cybersecurity in Belgium. [Connect with me on LinkedIn](https://www.linkedin.com/in/rayan-el-jattari-41a6353a2)

<div align="center">
<br>
<sub>Harden it · Attack it · Detect it · Document it</sub>
</div>
