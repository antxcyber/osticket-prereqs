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
<h2>Installing osTicket</h2>

- From the Installation Files, downaload and install <b>osTicket v1.115.8.zip</b>

- Extract the upload folder from the zip file and copy the folder into the directory
<b>C:\inetpub\wwwroot</b> in your VM
<img width="1215" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/65bad9c5-a9c6-444a-9026-e1e20e271d0d">
<p></p>
- After moving the upload file rename it to "osTicket"
- Go back to IIS and restart the server
- In IIS Manager, expand the connection <b>Sites</b> then <b>Default Web Sites</b> to click and highlight <b>osTicket</b>. Then, navigate to <b>Browse Folder</b> and click on <b>Browser*.80 (http)</b>
- The page of osTicket Installer should now pop up, if it does not, check your directories of your files and folders.
<img width="1215" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/c07ff257-a312-4a57-940f-57ef85f62a99">
- In IIS Manager, go to <b>osTicket</b> and click on <b>PHP Manager</b> and click on <b>Enable or Disable extensions</b> and enable the following
<p></p>
- php_imap.dll
<p></p>
- php_intl.dll
<p></p>
- php_opcache.dll
<p></p>
-Refresh osTicket Installer on your browser to see <b>PHP IMAP Extension</b> and <b>Intl Extensions</b> are checked signifying the extensions are installed
<p></p>
- After configurations locate the php file <b>ost-sampleconfig.php</b> inside the directory <b>C:\inetpub\wwwroot\osTicket\include\</b> and rename it to <b>ost-config.php</b> because osTicket Installer needs to interact with this file
<p></p>
-Now go to the <b>Properties</b> of the ost-config file and go the the <b>Advanced</b> settings in <b>Security</b> and <b>Disable Inheritance</b> to remove all inheritance permissions from the file (essentially making a "clean" object)
<p></p>
- Now add a new Permission, then click on <b>Select a principle</b> and for a new object type "everyone" then click on <b>Check names</b> to set the Group and click on OK. Then check all the boxes on Basic Permissions and then click OK. Now everyone using osTicket should have full permission to use it.
<p></p>
- Head to osTicket on your browser and click on <b>Continue</b> then set your <b>System Settings</b> and <b>Admin User</b> until you get to <b>Database Settings</b>
<p></p>
-For login information, you can set it to a fake email such as "yourname@helper.com", 
<p></p>
- From the <b>Installation Files</b>, download and install <b>HeidiSQL</b>
<p></p>
- Go through basic setup then launch HeidiSQL and create a New Session using the username "root" and password "Password1"
<img width="684" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/49dd50e7-c68e-4139-9950-e2487c3f8ff7">
<p></p>
- Create a Database and name it <b>osTicket</b>
<p>
- Once connected, go back to osTicket Installer type in our username (root) and password (Password1) into the respected fields in Database Settings
<p> 
-MySQL Database: osTicket
<p></p>
-MySQL Username: root
<p></p>
-MySQL Password: Password1
<p></p>
- Click <b>Install Now</b>, osTicket should now be fully installed on your VM!

<img width="1308" alt="image" src="https://github.com/antxcyber/osticket-prereqs/assets/148983947/8f88a6e6-1300-46c1-98f9-f5fd1f74930f">
