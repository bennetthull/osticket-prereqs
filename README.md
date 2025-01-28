<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS) W/ CGI
- Install Web Platform Installer
- Install C++ Redistributable
- Install MySQL and Set Up Username/Password
- Configure Permissions and Install oSTicket

<h2>Installation Steps</h2>

<p>
  <img width="599" alt="Screenshot 2025-01-23 at 10 37 30 PM" src="https://github.com/user-attachments/assets/56188130-d512-46b5-9bff-9b9621272c35" />
</p>
<p>
After creating a Windows 10 virtual machine in Azure, I used remote desktop to connect to it via its public IP address. From there, I enabled Internet Information Services (IIS) with CGI. I did this in Control Panel. This will act as a web server that will run on the computer. 
</p>
<br />

<p>
<img src="https://i.imgur.com/kC5I22k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the oSTicket installation files folder (obtained by aggregating oSTicket documentation) I installed PHP Manager for IIS, the Rewrite Module, and created the directory C:\PHP. I then unzipped PHP 7.3.8 into the "C:\PHP" folder. After that I installed the C++ Redistributable file "VC_redist.x86.exe"
<br />

<p>
<img src="https://i.imgur.com/oRUHDI0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, I installed MySQL 5.5.62. This will be the database that will store the user accounts, ticketing information, etc. inside oSTicket. After that I opened IIS as an Admin, registered PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe). Then I reloaded IIS (Open IIS, Stop and Start the server). I subsequently installed oSTicket from the oSTicket installation files folder. I did so by copying the upload folder into the web server folder. I loaded the osTicket site after that. I then enabled the missing extensions in IIS. Then I renamed ost-sampleconfig.php to ost-config.php and set full access permissions for "Everyone." I installed HeidiSQL, created a session with root/root, and created a database named osTicket. Then I finished the osTicket setup in the browser by entering the MySQL details and clicking "Install Now!"</p>
<br />
