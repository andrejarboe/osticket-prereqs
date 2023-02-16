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

- In this tutorial, we will be creating a Virtual Machine (VM) on the Microsoft Azure portal. 
- This VM will be a remote computer that we can use to protect our physical machine from any potential damage. To begin, we will create a resource group titled "osTicket". 
- Then, we will create a VM with 2-4 CPUs. 
- For the purpose of this example, I will be using 4 CPUs.

    ![Disk Sanitization Steps](https://i.imgur.com/OPaIGoN.png)  

- Once the VM is set up, you can use the public IPv4 address to connect to the VM using the Microsoft Remote Desktop Protocol (RDP).
- If you are a Mac user, you will need to download Microsoft RDP in order to connect to the VM.

    ![Disk Sanitization Steps](https://i.imgur.com/uLVKzxS.png)  

- Now that you have your VM up and running, you will need to enable IIS.
- Open the Control Panel, then select 'Uninstall a Program'.
- On the left, click 'Turn Windows Features On or Off'.
- A list will appear - click to enable Internet Information Services.

    ![IIS Setup](https://i.imgur.com/qtEnuWu.png)  

- Now that IIS has been set up, let's go ahead and install Web Platform Installer. 
- Here's the link: [Web Platform Installer and other Files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

- Clicking the link will give you access to everything needed to install osTicket. 
- Utilize the Web Platform Installer to get osTicket operational.

    ![IIS](https://i.imgur.com/AxHCfQ6.png)
