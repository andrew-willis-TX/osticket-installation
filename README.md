<h1> osTicket Installation </h1>

<p align="center">
<img src="https://yunohost.org/user/images/osticket_logo.svg" height="50%" width="50%" alt="osTicket Logo"/>
</p>

In this lab exercise we explore the ticketing software osTicket. This tutorial explains the set up process and requirements for osTicket to function properly. The neccessary additional software required can be found in the CourseCareers Installation Files. https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
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

8. Download and install MySQL. 

9. Open IIS as Admin. 

10. Register PHP within IIS  

11. Stop then Start the server within IIS. 

12. Download and install HeidiSQL. 


