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

- Set up an Azure Virtual Machine (VM) environment (Windows 10 4 vCPUs recommended)
- https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 (Download these files onto your Azure Virtual Machine)
- Install/Enable IIS in Windows
- Install Web Platform Installer
- Install MySQL
- Install C++ Redistributable
- Configure permissions and install osTickt
<h2>Installation Steps</h2>

<h2>Install / Enable IIS in Windows WITH
CGI and Common HTTP Features</h2>
<p>
<img <img width="1440" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/dcc15b8e-708d-4df6-9446-4fc1d8bef6ef">

</p>
<p>
- In your VM, go to the Control panel and head to Programs.
</p>
- Under Progam and Features click on Turn Windows features on or off
</p>
- Navigate the list and check the box for Internet Information Services, after doing so expand it.
<p></p>
- World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
<p></p>
- Expand Common HTTP Features and make sure all boxes are checked.

</p>
<br />

<p>
<h2>Installing Files for osTicket</h2>
- From the Installation Files, download <b>PHP Manager</b> and <b>Rewrite Module</b>
<p>
- Create a Folder in your VM's C Drive and name it <b>PHP</b>
<img <img width="893" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/2d11e6a0-614f-4974-b862-dc13d83c7792">
<p></p>
-From the Installation Files, download the zip file <b>PHP 7.3.8</b> then unzip the contents into the PHP folder we made (C:\PHP).
<p>
-From the Installation Files, download and install <b>VC_redist.x86.exe</b>, and <b>MySQL 5.5.62</b>

<H2>Setting up IIS and PHP</H2>
</p>
- Open <b>Internet Information Services (IIS) Manager</b> and run it as Administrator
</p>
- Go to <b>PHP Manager and click on Register new PHP Version</b>, set the directory to the <b>php-cgi</b> file found in the PHP folder we've set in the C Drive (C:\PHP)
<p></p>
<img <img width="703" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/4ca7baef-a682-4c07-91f1-975c09b83199">


</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
