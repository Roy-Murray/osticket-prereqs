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
- Install C++ Redistrutable
- osTicket installation files
- HeidiSQL

<h2>Installation Steps</h2>
<h3>Create a Virtual Machine</h3>
In Microsoft Azure we will create a VM and create a new resource group called "osTicket.

- Virtual: Machine Name "osTicket-vm"
- Image: Windows 10 pro, version 22h2 -x64 Gen2
- Size: 2vcpus, 8 gib memory
- Create a username and password for Adminstrator account


Check the licensing box and review & create the VM


![vm1](https://github.com/user-attachments/assets/d80efa40-8a41-474e-ae53-1382f6425442)

Open up Remote Desktop Connection
- Enter VM IP Address
- Log into VM with username and password
- Within the VM Download and unzip the osTicket-Installation-Files.zip onto your desktop

<h2>Enable IIS</h2>

- Open Control panel and click uninstall a progrsam
- Click on turn windows feauture on
- Click on IIS then world wide web services and check the box that says CGI


![image](https://github.com/user-attachments/assets/fd18fcee-b290-4479-8986-7983d3822275)




![image](https://github.com/user-attachments/assets/9fa8f414-b3de-4427-80b8-b603193035c0)




<h2>Install PHP Manager</h2>

- Go into osTicket Installation files
- Click PHP Manager then press next and agree
- Click rewrite_amd64 file and install it
- Create a folder in windows(C:) file explorer and name it PHP
- Go back to the php-7.3.8 folder and extract it to the PHP folder that was just created


 ![image](https://github.com/user-attachments/assets/52184a52-97c4-4959-8b12-c6536d554b32)



![image](https://github.com/user-attachments/assets/501119c8-cd2f-4915-a55a-c3dc7a2a3051)




![image](https://github.com/user-attachments/assets/58b9e00b-c6a2-4ae6-956d-4c9202324355)




<h2>Install C++ Redistrutable</h2>

- Double click The VC_redist file then agree and install


![image](https://github.com/user-attachments/assets/3af51d4f-3fd5-4f5b-a77d-c2487734e4a6)



<h2>Install Install MySQL</h2>

- Click mysql file in the osTicket-installionn files
- Click Next and accept, then next and typical and install.

![image](https://github.com/user-attachments/assets/f960cb3e-6d22-461e-9911-7517ad4d189d)

- Click standard configuration then next and next again

![image](https://github.com/user-attachments/assets/c639bc5f-40a1-4c9b-92fd-294aebe5441e)

- Enter root password then press next
- Execute and Finish

<h2>Configure IIS</h2>

- Open IIS as admin
- Open PHP Manager
- Register a new PHP version
- Provide path to php-cgi by opening the PHP folder and click the file
- Reload IIS byt clicking osTicket-vm and stop it then start.

![image](https://github.com/user-attachments/assets/44990591-c79f-4284-a61c-ba162695ce33)

![image](https://github.com/user-attachments/assets/4fdc6ddb-bbfb-4057-b88b-7c8b331e6e2c)

<h2>Install osTicket</h2>

- Go to osTicket installation files and extract it
- Copy the upload folder to the C:\inetpub\wwwroot folder
- Rename it to osTicket
- Reload IIS again
- Go to sites, then defualt web sites, lastly osTicket
- On the right click Browse .80


![image](https://github.com/user-attachments/assets/61b8333d-21db-4217-b158-356f544ba12b)

![image](https://github.com/user-attachments/assets/6109c3e1-694e-4d3b-86b9-0b470ad0adb6)

![image](https://github.com/user-attachments/assets/5e4d8640-0443-4db7-8622-2cfdcafb338e)

<h2>Enable Extensions</h2>

- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
- Enable: php_imap.dll
- Enable: php_intl.dll
- Enable: php_opcache.dll
- Refresh the osTicket site in your browser, observe the changes
  
![image](https://github.com/user-attachments/assets/3dcbfa4f-4434-44ee-aef3-44c716952c6b)

<h2>Rename: ost-config.php</h2>

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
- Assign Permissions: ost-config.php
- right click ost-config then press properties and click on the security tab
- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All


![image](https://github.com/user-attachments/assets/51e401d8-78a3-4991-b862-c8fb053e055b)

![image](https://github.com/user-attachments/assets/50eee0ba-da55-42e2-b778-57a11d23b33f)

<h2>Setting up osTicket</h2>

- go to the browser osticket setup site
- click continue
- Name Helpdesk
- Default email (receives email from customers)

![image](https://github.com/user-attachments/assets/4f267630-7b83-4e29-bd55-f6dafb0b21fb)

<h2>Install Heidi</h2>

- Open Heidi SQL from osticket installation folder
- Create a new session, root/root by selecting new and user: root and password: root and open
- Connect to the session
- Create a database called “osTicket”

  ![image](https://github.com/user-attachments/assets/8483673c-0cb6-41d1-a19b-e6226dcecc79)













