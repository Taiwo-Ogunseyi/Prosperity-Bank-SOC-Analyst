# Prosperity-Bank-SOC-Analyst

<h2>Description</h2>
Prosperity Bank has observed failed logins on Windows 10 and privilege escalation attempts on Ubuntu, indicating possible attacks. As a SOC analyst, investigate these incidents using Wazuh, report findings, and recommend mitigations such as pfSense VLAN segmentation to reduce lateral movement risks.<br/>

<h2>Languages and Utilities Used</h2>

- <b>Wazuh</b>
  <b>Ubuntu-VM</b>
  <b>Windows 10-VM</b>
  <b>Wireshark</b>
  <b>pfSense</b>

- <h2>Program walk-through:</h2>

- <h3> Phase 1: Simulation </h3>
1. Windows 10 Workstation
⚬ Perform repeated failed login attempts (6–8 times).

<p align="center">
Simulating Brute force attack on Windows 10 Workstation and its log capture in Event Viewer: <br/>
<img src="https://imgur.com/a/zhN766V" height="70%" width="70%" alt="network-setup" border="0">
<br />
<br />
The configuration phase: <br/>
<img src="https://i.ibb.co/5WYFt9S6/Screenshot-2025-07-31-215338.png" height="70%" width="70%" alt="Screenshot-2025-07-31-215338" border="0">
<br />
<br />
Initiating the process:  <br/>
<img src="https://i.ibb.co/dJbx6nFP/initiating-the-connection.png" height="70%" width="70%" alt="initiating-the-connection" border="0">
<br />
<br />
Network setup completed:  <br/>
<img src="https://i.ibb.co/7tt7kHGF/completed-network.png" height="70%" width="70%" alt="completed-network" border="0">
<br />
<br />
</p>


