# osticket-prereqs<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

-Web Server: Install a web server software such as Apache or Nginx on your Windows machine. In this tutorial, we'll use Apache as an example.

-PHP: osTicket requires PHP, so you'll need to install it. Download the latest version of PHP compatible with your system from the official PHP website (https://www.php.net/downloads.php). Make sure to choose the Windows installer for your architecture (32-bit or 64-bit).

-Database: osTicket relies on a database to store its data. Install a database server like MySQL or MariaDB on your Windows machine. For this tutorial, we'll use MySQL as an example.

-Text Editor: Choose a text editor to modify osTicket's configuration files. Notepad++ is a recommended option for Windows.

<h2>Step 1: Install and Configure Apache:</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download the Apache web server from the official website (https://httpd.apache.org/download.cgi). Choose the version compatible with your Windows architecture.

Run the installer and follow the on-screen instructions to complete the installation.

Once installed, open the Apache configuration file located at "C:\Apache24\conf\httpd.conf" (the path may vary depending on your installation).

Make the following changes in the configuration file:

Uncomment the line "LoadModule rewrite_module modules/mod_rewrite.so" by removing the "#" at the beginning.
Set the "DocumentRoot" directive to the folder where you want osTicket to be installed, e.g., "C:\Apache24\htdocs".
Enable directory listing by changing "Options None" to "Options Indexes FollowSymLinks" for the "DocumentRoot" directory.
Save the changes and restart Apache for the modifications to take effect.
<br />

  <h2>Step 2: Install and Configure PHP:</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Run the PHP installer you downloaded earlier and follow the installation wizard.

During the installation, choose the following options:

Select the installation directory (e.g., "C:\PHP").
Enable extensions: check the boxes for "mysqli" and "gd2" extensions.
After installation, locate the "php.ini" configuration file (e.g., "C:\PHP\php.ini") and open it with your text editor.

Make the following changes in the "php.ini" file:

Find the line with "extension_dir" and set it to "extension_dir = "C:\PHP\ext"".
Uncomment the line ";extension=mysqli" by removing the ";".
Uncomment the line ";extension=gd2" by removing the ";".
Save the changes and close the "php.ini" file.
</p>
<br />
 <h2>Step 3: Install and Configure MySQL:
</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download the MySQL Community Server installer from the official website (https://dev.mysql.com/downloads/installer). Choose the appropriate version for your Windows system.

Run the installer and follow the installation wizard to set up MySQL.

During the installation, choose the following options:

Select "Server Only" installation type.
Configure the MySQL root password.
Complete the installation process, and MySQL will be ready for use.

<h2>Step 4: Download and Install osTicket::</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Visit the osTicket website (https://osticket.com/) and click on the "Download osTicket" button to get the latest stable release.

Extract the downloaded osTicket ZIP file to the document root of your Apache web server (e.g., "C:\Apache24\htdocs\osticket").

Rename the "upload" directory to "osticket" (e.g., "C:\Apache24\htdocs\osticket\upload" becomes "C:\Apache24\htdocs\osticket\osticket").

In the "osticket" directory, locate the "include" folder and rename the "ost-sampleconfig.php" file to "ost-config.php".

Open the "ost-config.php" file with your text editor and configure the database connection settings by providing the MySQL database details (database name, username, and password).

Save the changes and close the "ost-config.php" file.
  </p>
<br />
 <h2>Step 5: Access osTicket:</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Launch your web browser and enter the following URL in the address bar: "http://localhost/osticket" (or replace "localhost" with the hostname or IP address of your server).

osTicket's web-based installer will guide you through the remaining setup steps, including creating an admin account and configuring email settings.

Follow the installer instructions to complete the setup.

Congratulations! You have successfully downloaded and installed osTicket on your Windows machine. You can now start using osTicket as a powerful ticketing system to manage customer support requests.
