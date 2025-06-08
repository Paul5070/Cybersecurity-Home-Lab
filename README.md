Cybersecurity Home Lab

Objective
The Cybersecurity Home Lab was built to simulate real-world attack scenarios using two virtual machines, Kali Linux (attacker) and Windows 10 (target). This lab provides hands-on experience in network scanning, payload generation, reverse shell exploitation, and both red team and blue team fundamentals. The primary goal is to demonstrate how system vulnerabilities can be exploited and how proper defensive mechanisms could mitigate such threats.

Skills Learned
1. Basic and intermediate penetration testing skills using Kali Linux
2. Manual IP configuration and virtual networking
3. Port scanning and enumeration using Nmap
4. Malware payload creation using msfvenom
5. Exploiting systems using msfconsole and Meterpreter
6. Understanding the risks of unsecured environments (e.g., disabled firewall)
7. Fundamentals of reverse shell techniques

Tools Used
1. VirtualBox or VMware
2. Kali Linux & Windows 10
3. Nmap port scanner, (Optional) Wireshark for traffic analysis
4. Metasploit Framework (msfvenom, msfconsole)
5. Setup Virtual Machines and configuration.
6. Splunk (SIEM)
Steps
Ref 1: Network Diagram
A home lab setup with two VMs: Kali Linux (Attacker) and Windows 10 (Target). IPs were manually configured for controlled communication.
![image](https://github.com/user-attachments/assets/a46e925c-bf13-4462-869d-87d872a9be4b)

Ref 2: Windows 10 Firewall Disabled
Windows firewall was turned off to demonstrate the importance of host hardening. This allows inbound connections from Kali without restrictions.
****![Cybersecurity Home Lab- Disabling Firewall Importance of security](https://github.com/user-attachments/assets/f772fd59-b842-4102-8231-276ce2a285c8)

Ref 3: Nmap Port Scan
Using nmap from Kali to enumerate open ports on the Windows 10 host.
![Cybersecurity Home Lab-Nmap Port scan 1](https://github.com/user-attachments/assets/7a2cf844-1690-4901-900e-50353541177e)

Ref 4: Payload Creation 
Creation of msfvenom payload, a tool within metasploit framework. The payload is designed to create a reverse TCP shell that connects back to the attackers Kali Linux Machine once executed on the WIndows 10 target.
![Cybersecurity Home Lab-msfvenom payload executable](https://github.com/user-attachments/assets/6dc3583b-48e1-4e95-9fbb-6291ad9e807f)

Ref 5: Exploiting Payload via Multi/Handler
The multi/handler in Metasploit was used to catch the reverse shell. Once the payload was run on the target, a Meterpreter session opened, confirming successful exploitation.
![Cybersecurity Home Lab-payload option have changed](https://github.com/user-attachments/assets/d813cf46-426b-4253-aff1-c3197ab0a8e0)
![Cybersecurity Home Lab-pushing malware through http server](https://github.com/user-attachments/assets/a0599de8-fea5-4626-8a4b-c9fe5c1d7ae8)

Ref 6: Established Connection for Exploitation
After the payload and using a simple Python HTTP server, the target system downloaded and executed Resume.pdf.exe. The multi/handler listener on Kali captured the reverse shell and successfully opened a Meterpreter session.
![Cybersecurity Home Lab-Established connection 2](https://github.com/user-attachments/assets/5f584500-db8b-494b-b0dc-4944661fcab2)

Ref 7: 
