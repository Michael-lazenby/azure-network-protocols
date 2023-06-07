# Azure-network-protocols

<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this project, I observed various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDP, DNS, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Created two virtual machines, one with Ubuntu and one with Windows 10
- Connected to the Windows VM using RDP
- Installed Wireshark on the Windows 10 machine
- Initiated a continous ping request to the Ubuntu machine 
- Added inbound port rules in the Ubuntu VM's network security group to deny ICMP traffic, and observed the ping request time out through Wireshark
- Removed inbound port rules and watched the ping requests reinitiate through Wireshark
- Used SSH to gain access to the Ubuntu machine and created a new directory
- Obsereved DNS and RDP traffic through Wireshark

<h1>Lab Summary</h1>
<h2>Creating virtual machines</h2>
<p>
This lab required me to use two virtual machines, one with Windows 10 and another with Ubuntu. I used Azure Network Watcher to confirm both of the VMs were connected to the same network.</p>
<img src="https://i.imgur.com/YK94SIh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<h2>Wireshark installation and observation</h2>
<p>
Before I started the lab I installed Wireshark. I observed network traffic with Wireshark, and I was also able to filter ports by using the filter bar. For example, I filtered ICMP(Internet Control Message Protocol) and viewed traffic between my virtual machines when I sent ping requests to the Ubuntu VM. After sending one ping request I sent a continuous ping request to the Ubuntu VM.
</p>
<br />

<p>
<img src="https://i.imgur.com/SDL7FsW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h2>Blocking inbound ports with port security rules</h2>
<p>
The next step of my project was to stop the continuous ping requests from my Windows VM. I did this by adjusting the inbound port rules for my Ubuntu VM via the Network Security Group settings, and I denied traffic from the ICMP port. This allowed me to observe the ping requests timing out, and I didn't receive a response from the VM. </p>
<img src="https://i.imgur.com/vbtVvOi.png" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Other port practice</h2>
<h3>Connecting with SSH</h3>
<p>
I connected to the Ubuntu VM using SSH. While connected to the Ubuntu VM I created a new directory using the mkdir command and added a file to the directory using the touch command. 
<img src="https://i.imgur.com/4RHnH8G.png" width="80%" alt="Disk Sanitization Steps"/>
<h3>DNS traffic monitoring</h3>
<p>
I used nslookup to send a DNS query to Google and observed the response through Wireshark. I made a DNS query to Google and received a response containing Google's IPv6 and IPv4 addresses.</p>
<img src="https://i.imgur.com/UB7QZNv.png" width="80%" alt="dns"/>

<br />
<h2>Alternative method to filter ports via Wireshark</h2>
<p>
I also learned a different method to filter ports in Wireshark. The other way to filter ports is by typing the network protocol and the port you are trying to filter. I have listed examples below:</p>

- tcp.port == 22
- udp.port == 53

<br />
<h2>Conclusion</h2>
<p> Overall this lab was insightful because it allowed me to visualize network traffic through different protocols. It allowed me to tinker with different settings and gain hands-on experience. It is important to read how network protocols work, but the hands-on experience reinforces the concepts I have been learning about. </p>
