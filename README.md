<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a virtual machine and complete all following actions within it-
- Enable Information Services
- Install web platform installer
- Install MySQL instead of username and password
- Install C++ Redistributable
- Configure permissions and install osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/qg7rdEw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For this tutorial I will be using Microsoft Azure. Begin by creating a Virtual machine on Azure and once that has been completed, you must log intot the VM with remote desktop.
</p>
<br />

<p>
<img src="https://i.imgur.com/5KePHSn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Head to the control panel by clicking the start button. Once the control panel is open click "Programs" and you should then see an option to "Turn windows features on or off". Once that option is selected you will be shown many of the different windows features. From there search for "Internet Information Services" and proceed by selecting it then clicking "OK". IIS has now been installed.
</p>
<br />

<p>
<img src="https://i.imgur.com/Xo2OZxC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
The next step is to then download and install "Web Platform Installer". Upon opening the program you must then download "MySQL 5.5" from within the program to which you will later create credentials for.
</p>
<br />

<p>
<img src="https://i.imgur.com/jzlbu5w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Make sure you add all simple versions of x86 PHP up until 7.3. You might also have a few failures so in order to resolve them you will have to install PHP version 7.3.8, PHP Manager 1.5.0 for IIS 10, and Microsoft Visual C++ 2009 Redistibutable Package.
</p>
<br />

<p>
<img src="https://i.imgur.com/bQC3dqu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You may now proceed to install osTicket v1.15.8, and once that is downloaded you must extract and copy the "upload" folder INTO c:\inetpub\wwwroot. After that the next step is to rename the "upload" folder to "osTicket" from within c:\inetpub\wwwroot.
</p>
<br />

<p>
<img src="https://i.imgur.com/8B9rhwN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS and then Stop and Start the server. Then go to "Sites" and click "Default" and then "osTicket". You should then see in the right side of the window "Browse *:80". That will route you to osTicket's page showing you what else is required to complete the install.
</p>
<br />

<p>
<img src="https://i.imgur.com/uBBE4dJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You should now see the three missing extensions. In order to fix this you must head back into IIS, click "sites", then "default", and lastly "osTicket". From there double click PHP Manager and then select "Enable or Disable an Extension". Enable the following; "php_imap.dll", "php_intl.dll", and "php_opcache.dll". 
</p>
<br />

<p>
<img src="https://i.imgur.com/XeDzkx1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Refresh the osTicket site in your browser and you should no longer have any missing extensions. Once completed head back into C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and rename it to "C:\inetpub\wwwroot\osTicket\include\ost-config.php".
</p>
<br />

<p>
<img src="https://i.imgur.com/8W2ql65.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now that it's renamed, its must be assigned permissions. Disable inheritance and then select "Remove All". After that select "New Permissions", then "Everyone", and "All". 
  
  
  
