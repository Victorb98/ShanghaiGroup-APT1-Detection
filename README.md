# 🕵🏾 ShanghaiGroup-APT1-Detection

🎯 *Advanced detection strategies for APT1 (Shanghai Group), leveraging host and network signals to target attacker tools and tactics.*

---

## 🧠 Who is Shanghai Group (APT1)?

Shanghai Group — aka **APT1** or **Comment Crew** is a Chinese state-sponsored threat group known for **long-term cyber-espionage** operations. They’ve been active against:

- 📡 Telecommunications  
- 🛩️ Aerospace  
- 🛡️ Defense  
- 💻 High-tech manufacturing  

🔍 Famously exposed in **Mandiant’s 2013 report**, APT1 remains a textbook example of Advanced Persistent Threat behavior.

---

## 📚 Understanding the Pyramid of Pain



> The more difficult the indicator is for an attacker to change, the more pain you inflict when you detect it.

🎯 **We’re targeting behaviour and tooling**, not just chasing rotating IPs and file hashes.

---![pyramid pain tryhackme image](https://github.com/user-attachments/assets/3870007d-8efb-4101-8e60-b91ff6fec8d8)


## 🔍 Indicators of Compromise (IOCs)

### 🔻 Easy for attackers to change:
- 🌐 IP addresses: often dynamic or leased  
- 🕸️ Domains: regularly updated (.ru, .top, etc.)  
- 🧱 File hashes: swapped with minimal effort  

### 🔺 High-impact detection (hard to change):
- 🧰 Tooling: Mimikatz, RATs, sideloading  
- 🧠 Behaviour: Lateral movement, PTH, DLL hijacking  
- 📡 C2 Patterns: Fake User-Agent strings and DNS activity  

---

## 🛠️ Detection Strategy

We focus on **host and network behaviour** where it hurts attackers. All rules are mapped to MITRE ATT&CK for real-world detection.

 🎯 Pyramid of Pain Mapping

| 🧩 **Detection Type**           | 🏗️ **Pyramid Level**       | 💥 **Pain to Attacker** |
|-------------------------------|----------------------------|--------------------------|
| 🌐 IPs / Domains              | Indicators                 | 🟢 Low                  |
| 🧱 File Hashes                | Hash Values                | 🟢 Low                  |
| 📡 DNS / User-Agent Detection| Network Artifacts          | 🟡 Medium               |
| 🧰 Mimikatz / DLL Hijacking  | Tools / Host Artifacts     | 🔴 High                 |
| 🧠 Lateral Movement + TTPs   | Tactics, Techniques & Procedures | 🔴 High         |

✅ Final Thoughts

🛡️ Detection Logic & Threat Focus
These detection rules are built to spotlight attacker behaviour, not just static IOCs, focusing on what adversaries do, rather than what they leave behind. Designed with blue teamers, SOC analysts, and threat hunters in mind, this approach emphasises real-world attack disruption.

🔍 Powered by MITRE ATT&CK mappings, the rules are aligned with common TTPs (Tactics, Techniques & Procedures) used by APT groups, ensuring the detections stay relevant and threat-informed.

🧠 Also, through my training on the Google Cybersecurity Certificate, I’ve developed practical skills in using tools like VirusTotal to analyse suspicious files, correlate indicators, and investigate potential threats, a skillset I actively applied in this project.

 💡 This project was inspired by a hands-on lab I completed on TryHackMe. 
 After working through a simulated APT detection challenge, I wanted to push myself further, to not just follow steps, but to understand *why* attackers do what they do, and how defenders can disrupt them at the behavioural level.  

 
This repository is the result of that challenge, a personal deep dive into APT1 (Shanghai Group) and how to detect it through real-world tactics, tools, and patterns.
<img width="1365" height="728" alt="Pyramid of pain tryhackme " src="https://github.com/user-attachments/assets/1f8dea0f-4e0b-4088-ba97-27712efc87b3" />

