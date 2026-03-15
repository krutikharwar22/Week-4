# Week-1
🛡️ **Final Project Report: Sentient Shield EDR Grid**
Internship Placement: Infotact Solutions – Cyber Defense Operations Center (CDOC)
Project Title: Enterprise EDR & Threat Hunting Grid Implementation
Team: Dinesh, Kruti, Aditi 
Date: 05/02/2026-5/03/2026

**1. Executive Summary**
During this 4-week internship, I led the implementation of Sentient Shield, a centralized Security Operations Center (SOC) and Endpoint Detection & Response (EDR) system. The project successfully transitioned Infotact from passive logging to Active Defense, providing real-time visibility and automated mitigation against ransomware and brute-force attacks across a hybrid (Linux/Windows) infrastructure.

**2. Weekly Technical Milestones & Deliverables**

**Week 1: Infrastructure & Agent Grid**

•	Wazuh Manager Deployment: Orchestrated a containerized Wazuh Manager via Docker, ensuring a scalable and isolated management environment.
![IMG1]
(C:\Users\Admin\Pictures p1.png)
 
•	Multi-Platform Integration: Successfully deployed and verified Agents on Ubuntu Server and Windows Server 2022.
•	Advanced Telemetry: Installed and configured Sysmon64 on Windows to capture high-fidelity process and network logs (T1059 - Command and Scripting Interpreter).

**Week 2: Detection Logic & Vulnerability Management**

•	File Integrity Monitoring (FIM): Configured real-time monitoring of critical directories (/etc/, C:\Windows\System32). Validated via PoC by creating/modifying files, resulting in alerts within 5 seconds.

Vulnerability Detection: Enabled the <vulnerability-detection> module using Canonical and MSU feeds.
o	Result: Identified 1,000+ high-risk vulnerabilities on the Windows node and critical CVEs (e.g., CVE-2022-3219) on Ubuntu.
 

 


 
•	Custom Rules: Developed Rule 100001 in XML to detect targeted brute-force patterns specific to Infotact’s environment.
 
**Week 3: Active Response (IPS)**
•	Automated Mitigation: Configured the firewall-drop active-response script.
•	The Scenario: If an SSH brute-force attack is detected (exceeding 5 failed attempts), Sentient Shield automatically bans the attacker's source IP for 1 hour.
•	Verification: Simulated an attack; verified the IP was successfully blocked in the host’s local firewall (iptables/netsh).
 

**Week 4: Threat Simulation & MITRE Mapping**
•	Adversary Simulation: Used Atomic Red Team techniques to simulate ransomware behavior (T1490 - Inhibit System Recovery).
 
•	Visualizing the Kill Chain: Mapped all alerts to the MITRE ATT&CK Framework on the Wazuh Dashboard, allowing the SOC team to visualize the attack from initial access to execution.
________________________________________
3. Evidence of Success (Audit Check)
|Goal	Evidence Found in Project	Status
Real-time FIM	Alerts generated for test.txt and /etc/ modifications	Verified ✅
System Visibility	Sysmon running on Windows; Wazuh Manager active	Verified ✅
Vulnerability Assessment	Full inventory of High/Critical CVEs mapped	Verified ✅
Custom Defense	XML Rule 100001 for "Bruce" (Brute-force) attacks	Verified ✅
|
________________________________________
**4. Professional Impact & Conclusion**
The implementation of Sentient Shield has fundamentally transformed the security posture at Infotact Solutions by significantly reducing both the *Mean Time to Detect (MTTD) and Mean Time to Respond (MTTR). By transitioning the infrastructure from passive logging to Active Defense, the project now provides autonomous, real-time protection against sophisticated threats like ransomware and brute-force attacks.
 Key Internship Takeaways
Through leading this deployment, I have gained critical experience in several core cybersecurity domains:
EDR Engineering: I developed a deep architectural understanding of XDR systems and the complexities of secure agent-manager communication across hybrid environments.
Incident Response: I moved beyond theoretical knowledge to bridge the gap between "seeing an alert" and "automatically stopping the threat" through automated IPS configurations
Risk Communication: I learned the vital skill of translating raw, technical CVE data into actionable patching priorities that enable the IT team to address the highest risks first.

**5. Appendices: Technical Verification Screenshots**

•	Figure 1: Wazuh Running Status Implemented Successfully
•	Figure 2: FIM Success on Ubuntu and Windows Nodes
•	Figure 3: Vulnerability Reports for Server Infrastructure
•	Figure 4: Custom Brute-Force Rule Configuration


  
