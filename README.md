<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step1: Create VM for Domain controller(DC) and client-1. 
- Step 2: Configure DC private IP address to static, set client-1 DNS setting to DC private IP address
- Step 3: Install Active Directory, create domain and configure for admin and users.
- Step 4: Setup remote desktop for non-admin users on client-1 and attempt connections.
<h2>Lab Visual Diagram</h2>
<P>
  <img width="548" alt="image" src="https://github.com/user-attachments/assets/9653c620-73bd-4805-be60-734e519b9a65" />
</P>
<h2>Deployment and Configuration Steps</h2>

<p>
<img width="929" alt="image" src="https://github.com/user-attachments/assets/839c63d4-f634-4e3d-af9b-8e3266e5b035" />
</p>
<p>
After we create our virtual machines, we need to set DC-1 server's ip address as "static" meaning it wont change. For this we would: click on virtual machines inside azure -> choose server (DC-1) -> Network settings -> IP configurations -> ipconfig1 -> static. (NOTE: in order for this test to run smoothly we will have to disable microsoft firewall by logging into DC-1).
</p>
<br />

<p>
<img width="675" alt="image" src="https://github.com/user-attachments/assets/075a7dc9-87d4-4410-8865-45a4d4785ccf" />
<img width="537" alt="image" src="https://github.com/user-attachments/assets/cf28d994-ae2f-46b4-b01c-29d410864785" />
</p>
<p>
In order to change the DNS server for client-1 we need to go to our virtual machines and click on client-1. From here we: click on Network settings -> DNS servers (under settings option) -> custom -> enter private address of DC-1 (for this example). This will reroute traffic to DC-1 instead of the default gateway given by azure. To confirm this we can log into client-1 and execute the command [ipconfig /all] and [ping 10.0.0.4] on powershell, in order to confirm the DNS configuration and connection.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
