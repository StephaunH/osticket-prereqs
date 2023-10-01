<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This guide will walk through the steps required to set up and install the open-source ticketing software, osTicket, within a virtual environment using Microsoft Azure.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Virtual Machine
- osTicket Installation Files: [Installation Files](https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- Heidi SQL

<br/>

<h2>Installation Steps</h2>

**Step 1: Create a virtual machine (VM) in Microsoft Azure**

- Create a resource group called "RG-osticket". Make sure to select the region nearest to you.
- Create a virtual machine called "vm-osticket"
  

<p>
<img src="https://i.imgur.com/SM4nDyl.png"/>
</p>

For a step-by-step guide on creating a VM in Microsoft Azure, please refer to my guide [here](https://github.com/StephaunH/StephaunH/blob/main)

<br />

**Step 2: Log into the VM using RDP**

- Go to the VM resource and copy the Public IP Address

<p>
<img src="https://i.imgur.com/qLeyOD3.png"/>
</p>

- Using Remote Desktop, paste the IP address and click "Connect"
- Select "More choioces" and choose "Use a Different Account"
- Sign in using the username and password for the VM

<p>
<img src="https://i.imgur.com/mavugz5.png">
</p>

<p>
<img src="https://i.imgur.com/qYspkfU.png"/>
</p>

<br/>

**Step 3: Configure IIS**

- Open the Control Panel, select "Programs", then select "Turn Windows features on or off"
<p>
<img src="https://i.imgur.com/7Dxax4j.png">
</p>

- Navigate to "Internet Information Services" and enable "Web Management Tolls" and "World Wide Web Services"
- Expand "World Wide Web Services", then expand "Application Development Features" and enable "CGI"
- Under "Common HTTP Features" make sure all options are enabled
- Select "OK" and allow to install

<p>
<img src="https://i.imgur.com/U7sgsoW.png">
</p>

<p>
<img src="https://i.imgur.com/mKDJYm1.png">
</p>

**Step 4: 
