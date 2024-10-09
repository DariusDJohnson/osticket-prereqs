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

  - PHPManagerForIIS_V1.5.0.msi
  - rewrite_amd64_en-US.msi
  - VC_redist.x86.exe
  - MySQL 5.5.62 

<h2>Installation Steps</h2>


</p>
<p>
1.) The 1st step is to create a virtual machine (VM) via Microsoft Azure. This is where osTicket will be installed. Once the VM is created and it is successfully deployed, login with it's public IP address and the login credentials we made for the VM when it was created.
</p>


![image](https://github.com/user-attachments/assets/7499a868-5be8-4927-a70b-991096beaad5) ![image](https://github.com/user-attachments/assets/49e3c0b8-9b6a-40f1-9854-d48d4a161232)


</p>
<p>
2.) Within the VM, download and install the "osTicket-installation-files.zip". This folder contains osTicket as well as the pre-requisits needed in order for us to use osTicket.
<p>




![image](https://github.com/user-attachments/assets/f069a28d-bac1-46da-8356-ab4a3eb6ed17) 


</p>
<p>
  3.) Install IIS (Internal Information Services) within windows as well as CGI
  - Control panel -> programs -> programs and features -> click "Turn Windows features on or off" on the left hand side. rom there, scroll down to Internal Information Services(IIS) -> World Wibe Web Services -> Application Development Features -> CGI


  
![image](https://github.com/user-attachments/assets/df2c87de-2f45-4068-b41f-04fec9d8ec05)


</p>
<p>  
4.) Next, from the "osTicket-Installation-files.zip" folder install SOME of the prerequisites that were mentioned before.
  
  - PHPManagerForIIS_V1.5.0.msi
  - rewrite_amd64_en-US.msi
  - VC_redist.x86.exe
  - MySQL 5.5.62 
</p>



![image](https://github.com/user-attachments/assets/71576842-d945-4bc3-8284-e071bb905b1f)



</p>
<p>
5.) When installing MySQL 5.5.62 you want to select typical setup -> launch configuration wizard(after install) -> standard configuartion -> enter the credentials for logging in and connecting osTicket to your SQL database.
<p>

<img width="346" alt="Screenshot 2024-10-08 at 2 59 13 PM" src="https://github.com/user-attachments/assets/87ceb3ee-a043-4e8f-9f70-beace5339e95">

<img width="346" alt="Screenshot 2024-10-08 at 3 01 01 PM" src="https://github.com/user-attachments/assets/f29dcf4d-b8d1-4aa1-bb0f-5657965bb717">







</P>
<P>
6.) Create the directory C:\PHP - From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
<P>


<img width="312" alt="Screenshot 2024-10-08 at 3 34 16 PM" src="https://github.com/user-attachments/assets/9a521b79-babe-4ec4-af89-86200733b222">



</p>
<p>
7.) Open IIS as an admin, register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe), and reload IIS (Open IIS, Stop and Start the server)
<p>


![Image 10-7-24 at 2 11 AM](https://github.com/user-attachments/assets/abf71983-2014-48e1-99a6-664007068648)



</p>
<p>
8.) Install osTicket v1.15.8 from the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”. Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<p>



<img width="295" alt="image" src="https://github.com/user-attachments/assets/b88722b1-96b9-45e4-a3f0-efbf87d391f8">  <img width="324" alt="image" src="https://github.com/user-attachments/assets/dd94c3af-0b4e-44ff-9581-b8cdd40791cc">  <img width="324" alt="image" src="https://github.com/user-attachments/assets/d9cbd025-381f-42df-80aa-a9c518f612f0">



</p>
<p>>
9.) Reload IIS. On the leeft hand side: Click the name of your VM (in my case it's "osTickeet-VM) Go to "Sites" -> Default Web Site -> osTicket -> "Browse*:80(http) on the right hand side
<p>

<img width="449" alt="Screenshot 2024-10-09 at 7 46 36 AM" src="https://github.com/user-attachments/assets/fac034ea-497a-4174-a2cd-6ca06baf5205">



</p>
<p>
10.) Note that some extensions are not enabled. Go back to IIS, sites -> Default -> osTicket and double-click PHP Manager. Click “Enable or disable an extension”and enable:

  - php_imap.dll
  - php_intl.dll
  - php_opache.dll


Refresh the osTicket site in your browser, observe the changes
<p>


![Image 10-7-24 at 2 18 AM](https://github.com/user-attachments/assets/c8faceff-7878-4b48-b6fa-b33aa0eacda8)



