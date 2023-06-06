# azure-network-protocols

<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Step 1
- Step 2
- Step 3
- Step 4

<h1>Lab steps </h1>
<h2>Creating virtual machines</h2>
<p>
<img src="https://i.imgur.com/YK94SIh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created two virtual machines to monitor traffic between eachother. The first virtual machine was a windows 10 machine and the second virtual machine was a linux machine. I used RDP(Remote Desktop Protocol) and SSH(Secure Shell) to communicate between the two machines.
</p>
<br />

<h2>Setting up environment </h2>
<p>
I used Wireshark to monitor traffic to monitor packets. For example, I used the ICMP(Internet Control Message Protocol) to monitor echo requests between both of my machines.
</p>
<br />

<p>
<img src="https://i.imgur.com/SDL7FsW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h2>Blocking ports wiht Azure firewall</h2>
<p>
The next step of my project was to block contious echo requests through Azure firewall. I did this by going to the Networking section of my second virtual machine which enabled me to change the inbound port rules for my machine. When changing the inbound port rules you are also able to change the priority of the rule which determines which rules are processed first.
</p>
<br />
<h2>Other port practice</h2>
<h3>Connecting with SSH</h3>
<img src="https://i.imgur.com/4RHnH8G.png" width="80%" alt="Disk Sanitization Steps"/>
<h3>DNS traffic monitoring</h3>
<img src=:"https://i.imgur.com/UB7QZNv.png" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p>
<img src="https://i.imgur.com/vbtVvOi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
