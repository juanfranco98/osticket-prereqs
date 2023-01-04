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
<img src="https://i.imgur.com/jzlbu5w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
uyfu ufuj f






