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

- Navigate to "Internet Information Services" and enable "Web Management Tools" and "World Wide Web Services"
- Expand "World Wide Web Services", then expand "Application Development Features" and enable "CGI"
- Under "Common HTTP Features" make sure all options are enabled
- Select "OK" and allow to install

<p>
<img src="https://i.imgur.com/U7sgsoW.png">
</p>

<p>
<img src="https://i.imgur.com/mKDJYm1.png">
</p>

- Ensure IIS is properly installed by searching for "127.0.0.1" in a web browser
- The page should look like this:

<p>
<img src="https://i.imgur.com/Y7Kq1uQ.png">
</p>

**Step 4: Download and install prerequisites**

- From the installation files provided in the prerequisites section, download PHP Manager (PHPManagerForIIS_V1.5.0.msi)
- Open the file from its download location and install 

<p>
<img src="https://i.imgur.com/hLlnJQR.png">
</p>

- Download and install the rewrite module (rewrite_amd64_en-US.msi)

<p>
<img src="https://i.imgur.com/rzqXjIg.png">
</p>

- Download PHP (php-7.3.8-nts-Win32-VC15-x86.zip)
- In File Explorer, create a folder called "PHP" in your main drive (default Windows(C:))

<p>
<img src="https://i.imgur.com/rVYJz1y.png">
</p>

- Extract the PHP zip file (php-7.3.8-nts-Win32-VC15-x86.zip) into the new PHP folder

<p>
<img src="https://i.imgur.com/wwmh6w4.png">
</p>

<p>
<img src="https://i.imgur.com/KuJoMBk.png">
</p>

- Download and install Microsoft Visual C++ Redistributable (VC_redist.x86.exe)

 <p>
 <img src="https://i.imgur.com/DIcxgDm.png">
 </p>

- Download and install MySQLserver
- Make sure the option to "Launch MySQL Instance Configuration Wizard" is checked

<p>
<img src="https://i.imgur.com/QsdOYFS.png">
</p>

- Select "Typical", then "Standard" configuration
- Create a root password

<p>
<img src="https://i.imgur.com/v1cd0ov.png">
</p>

- Execute and finish configuartion

<p>
<img src="https://i.imgur.com/9km3RCk.png">
</p>

**Step 5: Configure PHP Manager**

- In the Start menu, search for "Internet Information Services" (or "IIS")
- Run as administrator

<p>
<img src="https://i.imgur.com/zry0Dj9.png">
</p>

- Open PHP manager

<p>
<img src="https://i.imgur.com/8CMd8qS.png">
</p>

- Register new PHP version

<p>
<img src="https://i.imgur.com/NlPN7OD.png">
</p>

- Browse to the PHP folder created earlier and select the file "php-cgi"

<p>
<img src="https://i.imgur.com/EOhl7eb.png">
</p>

- Refresh the server by right-clicking the VM in the left navigation bar and selecting "Refresh"

<p>
<img src="https://i.imgur.com/4sHtSuh.png">
</p>
