<h1> osTicket Installation </h1>

<p align="center">
<img src="https://yunohost.org/user/images/osticket_logo.svg" height="50%" width="50%" alt="osTicket Logo"/>
</p>

In this lab exercise we explore the ticketing software osTicket. This tutorial explains the set up process and requirements for osTicket to function properly. The neccessary additional software required can be found in the CourseCareers Installation Files. https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6. Use "standard" or "typical" installation processes unless otherwise stated.
<h2> Environments and Tecnology Used </h2>

- Microsoft Azure VM
- Remote Desktop
- Internet Information Services

<h2> Operating System </h2>

- Windows 10 Pro

<h2> Installation Steps </h2>

1. Within the Azure portal, create a Windows 10 VM. I used two vcpu, I would recommend using 4 vcpu. 
<p align="center">
<img src="https://i.imgur.com/mC7wQzU.png" height="50%" width="50%" alt="Creating Windows 10 VM."/>
</p>
 
2. Enable Internet Information Services (IIS) with Common Gateway Interface.
<p align="center">
<img src="https://i.imgur.com/XkD2xpy.png" height="50%" width="50%" alt="Enabling IIS and CGI."/>
</p>

3. Download and install PHP Manager for IIS. 
<p align="center">
<img src="https://i.imgur.com/UV3dPJy.png" height="50%" width="50%" alt="Installing PHP manager."/>
</p>

4. Download and install Rewrite Module.
<p align="center">
<img src="https://i.imgur.com/O1zpiiE.png" height="50%" width="50%" alt="Installaing Rewrite module"/>
</p>

5. Create the directory C:\PHP.
<p align="center">
<img src="https://i.imgur.com/n1ZXuw1.png" height="50%" width="50%" alt="Creating PHP folder in C: drive"/>
</p>

6. Download and install PHP. Unzip the contents of the download into the C:\PHP folder created in the previous step.
<p align="center">
<img src="https://i.imgur.com/y5coN80.png" height="50%" width="50%" alt="Downloading and installing PHP."/>
</p>


7. Download and install VC resdistributable.
<p align="center">
<img src="https://i.imgur.com/4I7MODI.png" height="50%" width="50%" alt="Installing C++ Redistributable"/>
</p>

8. Download and install MySQL. 
<p align="center">
<img src="https://i.imgur.com/TfOy5Tc.png" height="50%" width="50%" alt="installing mySQL.">
</p>

9. Create a new mySQL Server Instance using the Configuration Wizard. Note the username is root. Create a password you will remember.
<p align="center">
<img sr="https://i.imgur.com/XWwUaVz.png" height="50%" width="50%" alt="Creating new mySQL server."/>
</p>

10. Open IIS as Admin. 
<p align="center">
<img src="https://i.imgur.com/dV2GUFm.png" height="50%" width="50%" alt="Run IIS as an Administrator."/>
</p>

10. Register PHP within IIS.
<p align="center">
<img src="https://i.imgur.com/Y4Eole4.png" height="50%" width="50%" alt="Registering PHP within IIS."/>
</p>

11. Use the .exe file in the C:\PHP directory.
<p align="center">
<img src="https://i.imgur.com/l68ScVK.png" height="50%" width="50%" alt="Setting up the PHP directory."/>
</p>

12. Within IIS, restart the server.
<p align="center">
<img src="https://i.imgur.com/gFRHvpk.png" height="50%" width="50%" alt="Restarting the server."/>
</p>

13. We will install and configure osTicket over the next several steps. Download the osTicket software from Installation Files.
<p align="center">
<img src="https://i.imgur.com/jKP718v.png" height="50%" width="50%" alt="Downloading osTicket."/>
</p>

14. Extract and copy the "upload" folder to c:\inetpub\wwwroot.
<p align="center">
<img src="https://i.imgur.com/GKvF9Qc.png" height="50%" width="50%" alt="Copying upload folder to c:\inetpub\wwwroot."/>
</p>

15. Within c:\inetpub\wwwroot, rename the "upload" folder to "osTicket".
<p align="center">
<img src="https://i.imgur.com/ao45xiH.png" height="50%" width="50%" alt="Rename "upload" folder to "osTicket"./>
</p>

16. Within IIS, restart the server.
<p align="center">
<img src="https://i.imgur.com/3FPGWvV.png" height="50%" width="50%" alt="Restarting the server."/>


17. Within IIS, go to Sites-> Default-> osTicket. Click Browse *.80.
<p align="center">
<img src="https://i.imgur.com/w1h5dop.png" height="50%" width="50%" alt="Browsing to the local osTicket Support Page."/>
</p>

18. Some extensions will not be enabled. 
<p align="center">
<img src="https://i.imgur.com/iimfuQJ.png" height="50%" width="50%" alt="Initially some osTicket extensions will not be enabled."/>
</p>

19. Within PHP Manager of IIS, Enable extensions.
<p align="center">
<img src="https://i.imgur.com/30lrYIy.png" height="50%" width="50%" alt="Enabling osTicket extensions in PHP."/>
</p>

20. Enable the following extensions: "php_imap.dll","php_intl.dll", "php_opcache.dll".
<p align="center">
<img src="https://i.imgur.com/azmGcuc.png" height="50%" width="50%" alt="Enabling osTicket extensions in PHP."/>
</p>

21. Refresh osTicket in the browser and observe the changes.
<p align="center">
<img src="https://i.imgur.com/tuu4KgZ.png" height="50%" width="50%" alt="Enabling osTicket extensions."/>
</p>

22. Within file explorer, find C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php. Rename this file by removing "sample" from the name. 
<p align="center">
<img src="https://i.imgur.com/Pl2B3mK.png" height="50%" width="50%" alt="Find the file C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php."/>
</p>
<p align="center">
<img src="https://i.imgur.com/71SZw0x.png" height="50%" width="50%" alt="Renaming file."/>
</p>

23. Assign permissions for the file that was just renamed.  Disable inheritance - Remove all inheritance. 
<p align="center">
<img src="https://i.imgur.com/hhfIng2.png" height="50%" width="50%" alt="Changing permissions for osTicket config file."/>
</p>

24. Add new setting, select new principal, "everyone"
<p align="center">
<img src="https://i.imgur.com/lT0suij.png" height="50%" width="50%" alt="Adding new permissions for everyone."/>
</p>

25. Select Full Control.
<p align="center">
<img src="https://i.imgur.com/QuJHlY1.png" height="50%" width="50%" alt="Allowing everyone to have full control."/>
</p>

26. Within, osTicket click Continue.
<p align="center">
<img src="https://i.imgur.com/KmPabKS.png" height="50%" width="50%" alt="Continuing to set up osTIcket."/>
</p>

27. Fill in the System Settings and Admin User fields. DO NOT continue installing osTicket.
<p align="center">
<img src="https://i.imgur.com/q7EtSu3.png" height="50%" width="50%" alt="Beginning the osTicket setup."/>
</p>

28. Download and install HeidiSQL.
<p align="center">
<img src="https://i.imgur.com/uu8Dond.png" height="50%" width="50%" alt="installing HeidiSQL."/>
</p>

29. Create a new HeidiSQL session, use the same password from the step 9. 
<p align="center">
<img src="https://i.imgur.com/k2kB8Os.png" height="50%" width="50%" alt="Creating new SQL session."/>
</p>

30. Create a new SQL database named "osTicket".
<p align="center">
<img src="https://i.imgur.com/ZZwXHyX.png" height="50%" width="50%" alt="Creating new database."/>
</p>

31. Fill in the remaining information to finish the osTicket installation. The username and password are the same from step 9. Click Install Now.
<p align="center">
<img src="https://i.imgur.com/weFLHwF.png" height="50%" width="50%" alt="Finishing the osTicket installation."/>
</p>

 


