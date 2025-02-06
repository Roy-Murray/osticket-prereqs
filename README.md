<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial is showcasing a guide to the prerequesites and installing of the open-source help desk ticketing system, osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Account
- Enable IIS
- Remote Desktop Access
- osTicket installation files
- HeidiSQL

<h2>Installation Steps</h2>
<h3>Create a Virtual Machine</h3>
In Microsoft Azure we will create a VM and create a new resource group called "osTicket.

- Virtual: Machine Name "osTicket-vm"
- Image: Windows 10 pro, version 22h2 -x64 Gen2
- Size: 2vcpus, 8 gib memory


Check the licensing box and review & create the VM.


![vm1](https://github.com/user-attachments/assets/d80efa40-8a41-474e-ae53-1382f6425442)


<h2>Install PHP Manager</h2>

- Go into osTicket Installation files
- Click PHP Manager then press next and agree

  ![image](https://github.com/user-attachments/assets/52184a52-97c4-4959-8b12-c6536d554b32)

- Click rewrite_amd64 file and install it

![image](https://github.com/user-attachments/assets/501119c8-cd2f-4915-a55a-c3dc7a2a3051)

- Create a folder in windows(C:) file explorer and name it PHP
- Go back to the php-7.3.8 folder and extract it to the PHP folder that was just created

![image](https://github.com/user-attachments/assets/58b9e00b-c6a2-4ae6-956d-4c9202324355)


