# Prosperity-Bank-SOC-Analyst

<h2>Description</h2>
Prosperity Bank has observed failed logins on Windows 10 and privilege escalation attempts on Ubuntu, indicating possible attacks. As a SOC analyst, investigate these incidents using Wazuh, report findings, and recommend mitigations such as pfSense VLAN segmentation to reduce lateral movement risks.<br/>

<h2>Languages and Utilities Used</h2>

- <b>Wazuh, </b>
  <b>Ubuntu-VM, </b>
  <b>Windows 10-VM, </b>
  <b>Wireshark, </b>
  <b>pfSense</b>

- <h2>Program walk-through:</h2>

- <h4> Phase 1: Simulation & Detection</h4>
Windows 10 Workstation - Perform repeated failed login attempts (6–8 times).

<p align="center">
Simulating Brute force attack on Windows 10 Workstation and its log capture in Event Viewer & Wazuh: <br/>
<img src="https://i.imgur.com/n3FVZPm.png" height="70%" width="70%" alt="network-setup" border="0">
<img src="https://i.imgur.com/FULq3Lo.png" height="70%" width="70%" alt="network-setup" border="0">
<img src="https://i.imgur.com/ODzzrzO.png" height="70%" width="70%" alt="network-setup" border="0">  
<br />
<br />

Ubuntu Server
<p align="center">
⚬ Run privilege escalation commands (sudo su,sudo -l).
<img src="https://i.imgur.com/FFxqXIf.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />
<p align="center">
⚬ Create a suspicious user (sudo useradd hacker).
<img src="https://i.imgur.com/XZY69vF.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />

- <h4> Phase 2: Network Activity & Capture</h4>

<p align="center">
⚬ Perform basic scanning and ping from kali to Windows
<img src="https://i.imgur.com/99tt1br.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<img src="https://i.imgur.com/Z1rDqG5.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />

<p align="center">
⚬ Perform basic scanning and ping from kali to Ubuntu.
<img src="https://i.imgur.com/1HhPjxW.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<img src="https://i.imgur.com/MgW1KAt.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />

- <h4> Phase 3: Mitigation </h4>
1. Propose Improvements
⚬ Configure pfSense VLAN segmentation with at least two VLANs:
<img src="https://i.imgur.com/lattrvL.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />

<p align="center">
￭ VLAN 1: Employee workstations (Windows).
<img src="https://i.imgur.com/iZu6Aoq.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<img src="https://i.imgur.com/wFW4fhf.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />
  
<p align="center">  
￭ Setting firewall rules for Windows Workstation VLAN
<img src="https://i.imgur.com/PnB3L39.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />

<p align="center">  
￭ VLAN 2: Backend servers (Ubuntu).
<img src="" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />

⚬ Monitor privilege escalation attempts and new user
creation events.



  
Initiating the process:  <br/>
<img src="https://i.ibb.co/dJbx6nFP/initiating-the-connection.png" height="70%" width="70%" alt="initiating-the-connection" border="0">
<br />
<br />
Network setup completed:  <br/>
<img src="https://i.ibb.co/7tt7kHGF/completed-network.png" height="70%" width="70%" alt="completed-network" border="0">
<br />
<br />
</p>


