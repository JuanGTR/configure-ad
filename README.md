<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create server and client VMs on Azure
- Ping server from client and allow ping on firewall
- Install AD DS on server and create domain and admin
- Change client DNS to server IP and join domain
- Create user accounts on domain using PowerShell
- Log into user accounts on client and verify AD management

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/xVNEbPm.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using Microsoft Azure, I set up two virtual machines: one as the server and the other as the client.
</p>
<br />

<p>
<img src="https://i.imgur.com/wAvxRzX.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
  I ensured connectivity between them by sending a ping through the private network from the client to the server. I had to allow the ping on the server’s firewall settings.
</p>
<br />

<p>
<img src="https://i.imgur.com/IjAyZOg.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the server computer, I installed active directory domain services and created a domain. I also created an admin account for the domain.
</p>
<br />

<p>
<img src="https://i.imgur.com/UWh3exb.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>

<p>
<img src="https://i.imgur.com/1l0WT0x.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<p>
On the client computer, I changed its DNS server settings in Azure to point to the server’s IP address. I also joined the client computer to the domain and enabled domain users to log into it.
</p>
<br />

<p>
<img src="https://i.imgur.com/zt4rXfF.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
Using Microsoft PowerShell as an admin, I created several user accounts on the domain to test it with. I logged into different user accounts on the client computer and verified that they were managed by the active directory on the server computer.
</p>
<br />




