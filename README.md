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
</p>
<p>
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<br />
</p>
<br />
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
