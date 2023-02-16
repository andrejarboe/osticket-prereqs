<p align="center">
    <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

This tutorial provides an overview of what is needed and how to install osTicket, the open-source help desk ticketing system.


## Environments and Technologies Used

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

## Operating Systems Used

- Windows 10 (21H2)

## List of Prerequisites

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

## Installation Steps

![Disk Sanitization Steps](https://i.imgur.com/OPaIGoN.png)  

- Create a Virtual Machine (VM) on the Microsoft Azure portal. 
- This VM will be a remote computer that we can use to protect our physical machine from any potential damage. To begin, we will create a resource group titled "osTicket". 
- Then, we will create a VM with 2-4 CPUs. 
- For the purpose of this example, I will be using 4 CPUs.

---

![Disk Sanitization Steps](https://i.imgur.com/uLVKzxS.png)  
- connect to the VM using the Microsoft Remote Desktop Protocol (RDP).
- If you are a Mac user, you will need to download Microsoft RDP in order to connect to the VM.

---

![IIS Setup](https://i.imgur.com/qtEnuWu.png)  
- Now that you have your VM up and running, you will need to enable IIS.
- Open the Control Panel, then select 'Uninstall a Program'.
- On the left, click 'Turn Windows Features On or Off'.
- A list will appear - click to enable Internet Information Services.

---

![IIS](https://i.imgur.com/AxHCfQ6.png)
- Now that IIS has been set up, let's go ahead and install Web Platform Installer. 
- Here's the link: [Web Platform Installer and other Files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- Clicking the link will give you access to everything needed to install osTicket. 
- Utilize the Web Platform Installer to get osTicket operational.

---

![IIS](https://i.imgur.com/JJ8bZeJ.png)
- Now launch Web Installer Platform
- Install MySQL 5.5
- Install PHP 7.3 
- Install C++ redistributable package
- Install PHP Manager for IIS.

---

![alt text](https://i.imgur.com/TUGiSKi.png")

- Download osTicket zip file
- Extract the file
- copy the "upload" folder into: C:\inetpub\wwwroot
- Rename the "upload" folder to "osTicket"

---

![alt text](https://i.imgur.com/4AkTkV0.png")

- Open IIS Manager 
- Restart the server
- Navigate to Sites->Default->osTicket
- Click "Browse*.80" on the right
- This will cause the osTicket webserver to open in your default browser.

--- 

![alt text](https://i.imgur.com/APZgUTT.png")
- Now we have to activate some extentions in IIS
- go to Sites->Default->osTicket
- double click on PHP manager, and then on "Disable or enable an extension".
    - Activate "php_intl.dll" & "php_opcache.dll"
    - then refresh the osTicket webserver and look for the changes
    - "Intl Extension" should now be enabled.

---

![alt text](https://i.imgur.com/1nYaYGe.png")
- in exploer go to  "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php"
- Rename this file to "C:\inetpub\wwwroot\osTicket\include\ost-config.php"
    - (you are just deleting "sample")
- Assign Everyone full permissions to the new ost-config.php file.
- Disable inheritance->Removeall New Permissions->Everyone->all

---

![alt text](https://i.imgur.com/RmVk3q5.png")
- now set up osTicke in your browser
- choose a name or your help Desk
- select a default email address
- For MySQl use:
    - username: root
    - password: what you made when you installed MySQL int he earlier step
- in flie exploer:
    - delete "C:\inetpub\wwwroot\osTicket\setup"
    - Set Permissions to “Read” only in "C:\inetpub\wwwroot\osTicket\include\ost-config.php 
- Login to the osTicket Admin Panel " http://localhost/osTicket/scp/login.php"

---

Now you are done :)