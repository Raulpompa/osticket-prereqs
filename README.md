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
<img src="" alt="osTicket"/>
</p>
<p>
  <p></p>
<img src=""  alt="osTicket"/>
</p>
<p>
  <p></p>
<img src="" alt="osTicket"/>
</p>
<p>
  <p>.</p> 
<img src="" alt="osTicket"/>
</p>
<p>
  <p></p>
<img src=""  alt="osTicket"/>
</p>
