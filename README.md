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

- PHP Manager for IIS
- Rewrite module
- PHP 7.3.8
- Redsit
- MySQL 5.5.62

<h2>Installation Steps</h2>


![image](https://github.com/user-attachments/assets/7499a868-5be8-4927-a70b-991096beaad5)  ![image](https://github.com/user-attachments/assets/49e3c0b8-9b6a-40f1-9854-d48d4a161232)




</p>
<p>
1.) The 1st step is to create a virtual machine (VM) via Microsoft Azure. This is where osTicket will be installed. Once the VM is created and it is successfully deployed, login with it's public IP address and the login credentials we made for the VM when it was created.
</p>




![image](https://github.com/user-attachments/assets/f069a28d-bac1-46da-8356-ab4a3eb6ed17)   ![image](https://github.com/user-attachments/assets/71576842-d945-4bc3-8284-e071bb905b1f)

</p>
<p>
2.) Within the VM, download and install the "osTicket-installation-files.zip". This folder contains osTicket as well as the pre-requisits needed in order for us to use osTicket.
<p>


  
![image](https://github.com/user-attachments/assets/df2c87de-2f45-4068-b41f-04fec9d8ec05)

</p>
<p>
  3. Install IIS (Internal Information Services) within windows as well as CGI
  - Control panel -> programs -> programs and features -> click "Turn Windows features on or off" on the left hand side.
  
  From there, scroll down to Internal Information Services(IIS) -> World Wibe Web Services -> Application Development Features -> CGI

  After this is done, from the "osTicket-Installation-files.zip" folder install:
  Php Manger
  Rewrite Module
  VC_Redsit
  MySQL5.5.62
</p>



</p>
<p>


