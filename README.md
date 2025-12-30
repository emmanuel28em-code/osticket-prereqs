<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) COMING SOON...

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

### 1. Infrastructure and Environment

* **Virtual Machine:** An Azure Virtual Machine running Windows 10 with 4 vCPUs.


* **Remote Access:** A Remote Desktop client to log into the virtual machine.



### 2. Core Software and Roles

* **Web Server:** Internet Information Services (IIS) enabled on Windows with the **CGI** feature active.


* **Database Management:** [MySQL 5.5.62](https://www.google.com/search?q=https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view%3Fusp%3Dshare_link) and [HeidiSQL](https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit) for database creation and management.


* **Runtime:** PHP 7.3.8 and the [Microsoft Visual C++ Redistributable (VC_redist.x86.exe)](https://www.google.com/search?q=https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view%3Fusp%3Dshare_link).



### 3. Required Extensions and Modules

* **IIS Modules:** PHP Manager for IIS and the URL Rewrite Module.


* **PHP Extensions:** The following extensions must be enabled within PHP Manager:
* `php_imap.dll` 


* `php_intl.dll` 


* `php_opcache.dll` 





### 4. Installation Assets

* **Files:** The [osTicket-Installation-Files.zip](https://www.google.com/search?q=https://drive.google.com/uc%3Fexport%3Ddownload%26id%3D1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD) folder, which contains the osTicket v1.15.8 source code and necessary installers.

<h2>Installation Steps</h2>

<p>
<img width="927" height="642" alt="image" src="https://github.com/user-attachments/assets/360196dc-4221-4dcd-88e2-94fc57474ce3" />
</p>
<p>
Create an Azure Virtual Machine Windows 10, 4 vCPUs. 2 vCPUs is also ok. Ensure that you keep passwords in a secure password manager. Choose a region that allows Windows 10 os (ex.EastUs2)
</p>
<br />

<p>
<img width="870" height="854" alt="image" src="https://github.com/user-attachments/assets/d70dd678-bf42-4ecb-b2b1-15beed9e6b35" />
</p>
<p>
Log in to your newly created Virtual Machine with Remote Desktop. Grab the public IP and enter it into the remote desktop app for Windows.  
</p>
<br />

<p>
<img width="2570" height="1532" alt="image" src="https://github.com/user-attachments/assets/81daf84a-0724-4f85-97ac-405ac103616b" />
</p>
<p>
Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
We will use the files in this folder to install osTicket and some of the dependencies.

</p>
<br />
</p>
<br />

<p>
<img width="2376" height="1336" alt="image" src="https://github.com/user-attachments/assets/20a8cef6-fab9-4f45-aa19-7f5c79779418" />
  <img width="822" height="746" alt="image" src="https://github.com/user-attachments/assets/6d2a9dc0-73f6-411c-aa9b-637cbf7c3d57" />

</p>
<p>
Install / Enable IIS in Windows WITH CGI. In Windows VM go to Control Panel > Uninstall Programs > Turn Windows features on/off > [X] Internet Information Services >
World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<br />
</p>
<br />

<p>
<img width="1352" height="1468" alt="image" src="https://github.com/user-attachments/assets/7323e0e6-1fda-47a1-9feb-d6c7631ec1ff" />
<img width="1370" height="1470" alt="image" src="https://github.com/user-attachments/assets/e25b07a9-923c-4005-98ed-27cbaec4f847" />
</p>
<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
  From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1850" height="1144" alt="image" src="https://github.com/user-attachments/assets/7754fac0-2aa0-4e18-acaa-87a72e3aa29e" />
</p>
<p>
Create the directory C:\PHP. Open a new File Explorer window > Open C drive - Windows (C:) > Create new folder named PHP.
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1748" height="1452" alt="image" src="https://github.com/user-attachments/assets/784fcabd-e845-4d10-9e9a-76ed0638947d" />
  <img width="1580" height="1472" alt="image" src="https://github.com/user-attachments/assets/5ae4fa93-25f6-4f3b-9a19-42d2eafe1ddf" />

</p>
<p>
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder.
  From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1708" height="1316" alt="image" src="https://github.com/user-attachments/assets/97c1f59f-21cd-4c98-b77d-038fa9222b1f" />
</p>
<p>
From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
  Note: Root password can not be reset, do your best to keep track. 
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1084" height="888" alt="image" src="https://github.com/user-attachments/assets/dd4728c1-85f0-4386-b2b0-810ad930af46" />
  <img width="2118" height="1224" alt="image" src="https://github.com/user-attachments/assets/4daf5435-a042-493b-9f05-1a90538b9926" />
  <img width="1722" height="996" alt="image" src="https://github.com/user-attachments/assets/dd43e970-7784-4be5-8fde-aae904f8d9b4" />
</p>
<p>
Open IIS and run as Admin. Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1706" height="1470" alt="image" src="https://github.com/user-attachments/assets/4e907299-4e81-4d0d-bed3-c12eda97ae05" />
  <img width="1608" height="1518" alt="image" src="https://github.com/user-attachments/assets/771a119c-375a-4033-af4d-c3f0a8a697a6" />
</p>
<p>
Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="2128" height="1226" alt="image" src="https://github.com/user-attachments/assets/f3cf2394-f676-43a5-b1b8-6912df62bbce" />
  <img width="2870" height="1686" alt="image" src="https://github.com/user-attachments/assets/86640660-5935-43de-823a-b26e7eba9a54" />
</p>
<p>
Reload IIS (Open IIS, Stop and Start the server)  Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1438" height="1600" alt="image" src="https://github.com/user-attachments/assets/2d37256b-bfa1-4083-9500-677a802fa23d" />
  <img width="1012" height="1024" alt="image" src="https://github.com/user-attachments/assets/a0e93d43-18fc-4875-be9b-4e693a0ac396" />
  <img width="1198" height="1336" alt="image" src="https://github.com/user-attachments/assets/362dcbe6-3b45-453d-a764-01cb6780731f" />
</p>
<p>
Note that some extensions are not enabled. Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager. Click “Enable or disable an extension” Enable: php_imap.dll Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1562" height="994" alt="image" src="https://github.com/user-attachments/assets/8aafc165-be6f-4590-98d2-a4afb0fccdd6" />
  <img width="1524" height="1028" alt="image" src="https://github.com/user-attachments/assets/d040638c-3658-4799-bd08-56d3f530ca97" />
  <img width="964" height="598" alt="image" src="https://github.com/user-attachments/assets/dec94b35-0103-4daa-9f3d-21ebb8782905" />
</p>
<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
Assign Permissions: ost-config.php - Disable inheritance -> Remove All - New Permissions -> Everyone -> All
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1394" height="1388" alt="image" src="https://github.com/user-attachments/assets/8d611ceb-cc57-4a80-95b1-059a069b4ca7" />
</p>
<p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
<p>
<img width="1352" height="1390" alt="image" src="https://github.com/user-attachments/assets/5a0b4629-6c61-402d-b9ba-d4d5bc470821" />
  <img width="1354" height="946" alt="image" src="https://github.com/user-attachments/assets/b379341c-ec1c-44ad-b155-7be9b3b9b95c" />
  <img width="1838" height="1136" alt="image" src="https://github.com/user-attachments/assets/f7f7414a-f1cd-4f74-81d0-41ec1790eaa8" />
</p>
<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL. - Open Heidi SQL Create a new session, - root/root Connect to the session - Create a database called “osTicket”
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1132" height="726" alt="image" src="https://github.com/user-attachments/assets/b66774b2-8a8b-4413-9bc7-ae8673cc990d" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img width="1132" height="726" alt="image" src="https://github.com/user-attachments/assets/715f26de-e303-40ba-9b30-0a8c669165e5" />
</p>
<p>
Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />
<p>
<img width="1222" height="1272" alt="image" src="https://github.com/user-attachments/assets/1ae91725-51e6-4517-b9fa-921cdaaaf063" />
</p>
<p>
Congratulations, hopefully it is installed with no errors!
Browse to your help desk login page: http://localhost/osTicket/scp/login.php

