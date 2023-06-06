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

- Created 2 virtual machines, one with Ubuntu and one with Windows 10
- Connected to the Windows VM using RDP
- Installed Wireshark on the Windows 10 machine
- Initiated a continous ping request to the Ubuntu machine, Added inbound port rules in the Ubuntu VM's network security group to deny ICMP traffic, and observed the ping request time out through Wireshark.
- Removed inbound port rules and watched the ping requests reinitiate through Wireshark
- Used SSH to gain access to the Ubuntu machine and created a new directory
- Obsereved DNS and RDP traffic through Wireshark

<h1>Lab steps </h1>
<h2>Creating virtual machines</h2>
<p>
<img src="https://i.imgur.com/YK94SIh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I created two virtual machines first one withWindows 10 and the seocnd one with Ubuntu. After creating both virtual machines I made sure they were both on the same network via Network Watcher.
</p>
<br />

<h2>Environment setup</h2>
<p>
Before starting the lab I had to installed Wireshark. Once Wireshark was downloaded I was able to observe network traffic and I was also able to filter ports by using the filter bar. For example, I filtered ICMP(Internet Control Message Protocol) and was able to view traffic between both of my virtual machines when I sent ping requests. After viewing one ping request I sent a continous ping request to the Ubuntu machine.
</p>
<br />

<p>
<img src="https://i.imgur.com/SDL7FsW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h2>Blocking inbound ports with port security rules</h2>
<p>
The next step of my project was to stop the continous ping requests from my windows machine. I adjusted the inbound port rules for my Ubuntu machine via the Network Security Group and I denied traffic from the ICMP port. After observving the ping requests time out because of the port rules I changed the rules again changed the settings to allow ping requests again.
</p>
<img src="https://i.imgur.com/vbtVvOi.png" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Other port practice</h2>
<h3>Connecting with SSH</h3>
<img src="https://i.imgur.com/4RHnH8G.png" width="80%" alt="Disk Sanitization Steps"/>
<h3>DNS traffic monitoring</h3>
<img src="https://i.imgur.com/UB7QZNv.png" width="80%" alt="dns"/>
<br />

<p>
</p>
