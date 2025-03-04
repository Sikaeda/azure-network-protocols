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

- Create a windows and ubuntu virtual machine
- Observe traffic using wireshark
- 
- Step 4

<h2>Actions and Observations</h2>

![image](https://github.com/user-attachments/assets/d4e59fad-39d1-4ee4-a08d-ea8287e1bb68)

<p>
Create a Resource Group
Create a Windows 10 Virtual Machine (VM)
While creating the VM, allow it to create a new Virtual Network (Vnet) and Subnet
Create a Linux (Ubuntu) VM
While creating the VM, select the previously created Resource Group and the Virtual Network MUST BE THE SAME.
Authentication type: Username/Password
Ensure both VMs are in the same Virtual Network / Subnet


</p>
<br />

![image](https://github.com/user-attachments/assets/c41ff960-52f3-4fe6-a841-9d1280f54e56)
![image](https://github.com/user-attachments/assets/27013f3f-08c9-43e2-9b90-1fb84bbc9f50)

<p>
(Observe ICMP Traffic)
If using Mac, install Microsoft Remote Desktop
Use Remote Desktop to connect to your Windows 10 Virtual Machine
Within your Windows 10 Virtual Machine, Install Wireshark
Open Wireshark and start packet capture
Within Wireshark, filter for ICMP traffic only
Retrieve the private IP address of the Ubuntu VM (linux-vm) and attempt to ping it from within the Windows 10 VM
Observe ping requests and replies within WireShark
From The Windows 10 VM, open command line or PowerShell and attempt to ping a public website (such as www.google.com) and observe the traffic in WireShark

</p>
<br />

![image](https://github.com/user-attachments/assets/d8449f7c-298f-4b1d-a648-4948b369cbed)
![image](https://github.com/user-attachments/assets/5bcc7be7-f3c8-4fb8-93ad-ae8ce1d93dba)

<p>
Look up and use different commands in windows powershell/command prompt to do continuous pings. Configure firewall to block pings on the linux machine and attempt to ping the linux virtual machine again using the windows virtual machine. Observe other types traffic like DHCP, DNS, etc
</p>
<br />
