<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
In this lab, I'll provide a step-by-step guide to installing open source osTicket, a helpdesk ticketing system, on a Windows 10 VM in Azure. We'll configure IIS, PHP, and MySQL to support osTicket and complete the installation by securing it through permission adjustments and the removal of setup files. In the next lab, I'll cover post-installation configurations to demonstrate how to use osTicket as an admin, support team member, and end user.<br />


<!--<h2>Video Demonstration</h2>
IN PROGRESS 
<!-- I'll be compleating this in the future
- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com) -->

<h2>Environments and Technologies Used</h2>

- Microsoft Azure: For hosting the Windows 10 Virtual Machine.
- Windows 10: As the operating system for the VM.
- Internet Information Services (IIS): A web server to host the osTicket application.
- PHP: For server-side scripting to run osTicket.
- MySQL: As the database management system to store ticket data.
- HeidiSQL: A tool for managing and creating MySQL databases.

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Microsoft Azure Account: To create and manage the Windows 10 Virtual Machine.
- Windows 10 VM: With at least 4 vCPUs and Remote Desktop access enabled.
- osTicket Installation Files: Including osTicket v1.15.8, PHP, MySQL, PHP Manager, URL Rewrite Module, and HeidiSQL.
- Internet Information Services (IIS): Enabled with CGI support.
- PHP 7.3.8: Configured to work with IIS.
- MySQL 5.5.62: Installed and configured for osTicket.
- Remote Desktop Client: To connect to the Azure VM.

<h2>Installation Steps</h2>

<p>
  <p>Will start by creating a new VM to install osTicket.</p>
<img src="https://i.imgur.com/cHfxEnu.png" alt="osTicket"/>
</p>
<p>
  <p>How to set up your VM.</p> 
<img src="https://i.imgur.com/OsCV4O0.png" alt="osTicket"/>
</p>
<p>
  <p>DON'T FORGET TO CHECK THIS BOX!</p>
<img src="https://i.imgur.com/fD07nO1.png"  alt="osTicket"/>
</p>
<p>
  <p>After the VM has been crerated we can open it with it's IP through Remote Desktop.</p>
<img src="https://i.imgur.com/RJ8UAMX.png" alt="osTicket"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/sJPEXHm.png" alt="osTicket"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/WedLd2r.png"  alt="osTicket"/>
</p>
<p>
  <p>After connecting to the VM, I'll begin by downloading the osTicket zip file and extracting its contents. Next, I'll activate IIS (Internet Information Services) by going to Control Panel > Programs > Turn Windows Features On or Off. I'll then enable Internet Information Services, followed by World Wide Web Services > Application Development Features, and make sure to enable CGI as well.</p>
<img src="https://i.imgur.com/LMO1zsQ.png" alt="osTicket"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/ChpQLeU.png" alt="osTicket"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/ppSIToH.png"  alt="osTicket"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/DjiELqd.png" alt="osTicket"/>
</p>
<p>
  <p>To verify that the web server was installed successfully, I'll enter the loopback IP (127.0.0.1) in a web browser. If everything is set up correctly, the default IIS page should appear.</p> 
<img src="https://i.imgur.com/ipLV0ZC.png" alt="osTicket"/>
</p>
<p>
  <p>Next, I need to set up PHP Manager for IIS installation.</p>
<img src="https://i.imgur.com/aSvccSS.png"  alt="osTicket"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/JJ4dSpQ.png" alt="osTicket Install"/>
</p>
<p>
  <p>Download IIS URL Rewrite Module.</p> 
<img src="https://i.imgur.com/guO5Eeo.png" alt="osTicket Install"/>
</p>
<p>
  <p>After the installations are complete, I'll set up a PHP directory on the C drive by creating a new file and naming it PHP.</p>
<img src="https://i.imgur.com/491UvPK.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Next, I'll download PHP and unzip the file into the PHP directory I just created.</p>
<img src="https://i.imgur.com/bd97pcK.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/jNfqvEw.png" alt="osTicket Install"/>
</p>
<p>
  <p>I'll now download Microsoft Visual C++</p>
<img src="https://i.imgur.com/vuMuixB.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Next, I'll download MySQL.</p>
<img src="https://i.imgur.com/8zBvQh3.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/Br0WJ02.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/fBxoN1b.png"  alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/iqajpws.png" alt="osTicket Install"/>
</p>
<p>
  <p>Now I'll set up the login credentials and make a note of them for this project. However, it's important to avoid writing down passwords in real-world scenarios.</p> 
<img src="https://i.imgur.com/Tx8sFSX.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/TWT8jBT.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Launch IIS with administrative privileges.</p>
<img src="https://i.imgur.com/xdJvjDL.png" alt="osTicket Install"/>
</p>
<p>
  <p>Next, navigate to PHP Manager > Register New PHP Version and select the displayed file.</p> 
<img src="https://i.imgur.com/uDibguW.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/Mdvwz8s.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Return to the osTicketVM Home and click Restart under Manage Server on the right-hand side, Or Stop and Start.</p>
<img src="https://i.imgur.com/k1KrRkP.png" alt="osTicket Install"/>
</p>
<p>
  <p>Next, I'll download osTicket and copy the upload folder into the wwwroot folder within the inetpub directory.</p> 
<img src="https://i.imgur.com/spRYoJH.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/7LoCGWI.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Naming this file correctly is very important, or else it WON'T WORK! It should be named "osTicket" with no space between os and Ticket."</p>
<img src="https://i.imgur.com/SHiwQ9o.png" alt="osTicket Install"/>
</p>
<p>
  <p>Reload IIS and restart the server as I did earlier, then click on Browse *80 (http) on the right-hand side.</p> 
<img src="https://i.imgur.com/wO70ltS.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/9FKGe1C.png"  alt="osTicket Install"/>
</p>
<p>
  <p>After clicking on Browse *80 (http) on the right side of IIS, this page osTicket Installer should open if you followed all the steps correctly.</p>
<img src="https://i.imgur.com/wEqTSo9.png" alt="osTicket Install"/>
</p>
<p>
  <p>You'll notice that some extensions are not enabled. I'll enable a few of them in IIS. First, go to Sites > Default Web Site > osTicket. Then click PHP Manager > Enable or Disable an Extension. Enable php_imap.dll, php_intl.dll, and php_opcache.dll.</p> 
<img src="https://i.imgur.com/9JlDXZZ.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/qqlFfYQ.png"  alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/BmR6oOf.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/dFnDUF9.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/CBcSZlB.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Notice the changes.</p>
<img src="https://i.imgur.com/lFnTGSq.png" alt="osTicket Install"/>
</p>
<p>
  <p>Next, open File Explorer and navigate to C drive > inetpub > wwwroot > osTicket > include. Find the ost-sampleconfig.php file and remove the "sample" from the filename.</p> 
<img src="https://i.imgur.com/xHfFhm8.png" alt="osTicket Install"/>
</p>
<p>
  <p>Remove "sample" from ost-smapleconfig.php.</p>
<img src="https://i.imgur.com/KU5cujp.png"  alt="osTicket Install"/>
</p>
<p>
  <p>Right-click on ost-config.php > Properties > Security > Advanced, then click Disable Inheritance and select "Remove all inherited permissions from this object."</p>
<img src="https://i.imgur.com/EJe6owy.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/P05linM.png" alt="osTicket Install"/>
</p>
<p>
  <p>Click the Add button to add permissions to the file. Select a principal, type "Everyone," then click Check Names and okay. Check all the permissions, then click okay, Apply, and finally okay.</p>
<img src="https://i.imgur.com/Pyti0wC.png"  alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/v7Wh7Db.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/Xaq5jcO.png" alt="osTicket Install"/>
</p>
<p>
  <p>Click Continue on the osTicket web page in the browser and complete the setup page.</p>
<img src="https://i.imgur.com/2I5Vsv7.png"  alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/7MTrXEj.png" alt="osTicket Install"/>
</p>
<p>
  <p>Before setting up the database, we need to connect to it using HeidiSQL. Install HeidiSQL using the setup links provided.</p> 
<img src="https://i.imgur.com/UZTwwPp.png" alt="osTicket Install"/>
</p>
<p>
  <p>In HeidiSQL, click New, then set the Username = "root" and the Password = "ROOT" (using the MySQL password from the MySQL setup). Finally, click Open.</p>
<img src="https://i.imgur.com/SMJBJsQ.png"  alt="osTicket Install"/>
</p>
<p>
  <p>In HeidiSQL, right-click on Unnamed, select Create, then New Database. Name it "osTicket" and click okay. Afterward, continue filling out the database section of the osTicket setup. When finished, click Install Now.</p>
<img src="https://i.imgur.com/PTPxJ1o.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/Y3cHPbr.png" alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/aj5Xnxn.png"  alt="osTicket Install"/>
</p>
<p>
  <p></p>
<img src="https://i.imgur.com/oJJZlDQ.png" alt="osTicket Install"/>
</p>
<p>
  <p></p> 
<img src="https://i.imgur.com/UMZXtJ9.png" alt="osTicket Install"/>
</p>

  <p>For the final steps, go to C drive > inetpub > wwwroot > osTicket, locate the setup file, and delete it. Then, navigate to C drive > inetpub > wwwroot > osTicket > include, right-click on ost-config.php, and go to Properties > Security > Advanced. Select "Everyone," click Edit, and only check "Read & Execute" and "Read." Apply the settings.</p>

<h2>osTicket Installation Complete</h2>
<p>osTicket is now successfully installed and ready to use! In the next osTicket repository (Post-Installation Configuration), I'll guide you through configuring agents, their permissions and access, users, and much more!</p>
