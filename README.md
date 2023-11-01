<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

We are starting the demonstration with the fact that the Virtual Machine and Resource Group have already been created in Azure. 

There are alot of steps in this demonstration. I hope to walk you through the process and with supporting print screens and instructions. 

<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create a Resource Group in Azure (already installed)
- Create a Virtual Machine (VM) in Azure (already installed)
- Open Installation Files Link (holds downloads for installing)
  
Install various prerequisites '🖥️

    💡 Install/Enable IIS in Windows
   
    💡 Intall PHP Manager for IIS

    💡 Install Rewrite Module

    💡 Install PHP.7.3.8

    💡 Install MySQL 5.5.62

    💡 Install osTicket 

    💡 Install HeidiSQL


<h2>Installation Steps</h2>

We are going to Remote Desktop into newly created VM

Go to Azure and copy Public IP Address of VM 

 ![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/62e6d700-f50c-4b26-9383-10b6f1e8efd7)

Go to Start menu and type in: Remote Desktop - paste copied IP address -  Click Connect 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/5acf87ff-8ec3-47f4-924f-1d9895b8c7fe)

Go to Google Drive (Installation File Link) where downloads have been saved

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/57ba7425-ca0c-4b67-a999-f1a6f7184d0d)

Click on Use a different account and enter credentials from your virtual machine in Azure

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f465fd23-a76d-41ee-bb89-27182c664600)
![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/5df66413-7e03-42bc-ae08-a3b20958a9fa)

Right Click on Start Menu - Type run: 

Click on Programs 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/99d0fd85-55bb-4d6e-abeb-27068b5737ac)

Click on Turn Windows features on or off

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/e50c71ea-e6db-4717-a2cd-2e12da5e17d8)

Install/Enable IIS (Internet Information Services) in Windows WITH

CGI and Common HTTP Features

AND IIS Management Console

World Wide Web Services -> Application Development Features ->

[X] CGI

[X] Common HTTP Features


Search for Internet Information Services

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/7d040d18-985f-4e44-9902-10c3aa755b2b)

Click on the expand icon 

'💡And then click on World Wide Web services

'💡Under Application Development Features – Click on CGI

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b894c9aa-95bc-4748-bf29-fda1e498267b)


Under Common HTTP Features, make sure all the boxes are checked

Click OK

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/1738c350-c165-4b31-9496-a37d2ecf5802)

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/ebbfa26d-476f-42a2-a1f4-0e25b2e46f4f)

We are now going to check to see if IIS is installed. Go to a browser and type in 127.0.0.1

This page should appear 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f42d97e1-04b6-4f70-95a9-dc2be73801d1)


Default IIS is now running 

Next we are going to download PHP Manager - go to intstallation files right click on PHPManagerforIIS 

Click download anyway

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b454153d-6ce4-49d0-975b-479264dab93e)

Click Next

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/163cab67-0420-4b9d-8d7c-72760536e660)

Click on I agree

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/ae2487ab-948c-44c6-92a6-f1b45077d9f5)

Installation is complete. Click Close 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/cecbee98-0f9f-413d-895d-6b68e759d49f)

Install Rewrite Module: (Once again go to Installation Files Folder) and select rewrite_amd64_en-US and paste in browser

Click on rewrite_amd64_en-US to continue downloading 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/266161b0-b5be-4afb-8e79-95217f2efdae)

Click on box: I accept the terms in the License Agreement

Click Install

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/80fa8954-a792-4c07-bce3-8cc52c9b12cd)

Click Finish 

Next, we are going to create a directory C:\PHP

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/8ea23f44-8dae-4c50-9afd-d163019855c7)

Add a new folder – PHP

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/dce04c88-6b5a-4e39-97bf-b0c468dec61b)

To zip 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/4deff7b2-a8b6-492a-a3a1-84a3d901c772)

Right click  on       and select install 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/cfca7aee-5b53-4f96-b7ba-29deadb505cd)

Browse to C drive/PHP

Click select folder - extract 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/d9066ce6-a8e1-4687-92f8-9a802c62373c)

Next we are going to install VC redist

Once again we are going to dowload from the Google Installation file  

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f0876cfd-3563-437b-ad4a-689a930cf627)

Click on download anyway

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f4a7e428-565d-4837-801e-271e01801c3b)

Double click on  ![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/d800038f-4e49-4ffd-943e-40ea5b112e45)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b86d69cc-e36a-4288-a3ed-2fad41b42fa2)

Click on box – I agree to the license terms and conditions
Click Install 

Next we are setting up MYSQL

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/d8fa88a1-c008-467b-b030-466f47fc8850)

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/d73b3087-a5e0-4cb0-9936-f6bae9a0a1f6)

Once the setup is sucessful, then it's time to download

Go to downloads folder and select ![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/3869fcaa-7151-4923-834f-e02aed192ae1)

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/e72ee54c-4ecb-463a-b8d1-e9925756a5a3)

Click on next 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/cb36ce8e-2c93-4909-8c77-45d55f4beb1b)


Click on I accept the terms in the License Agreement

Click Next  

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/30072c94-593c-464e-90bc-0f0691fb2d01)

Click on typical

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/cc035f74-dccc-4f94-a95d-b5ed5860bb5a)

Next click on Install

Click Finish 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/fdb7ec6a-4293-490d-ad48-38e7f2676d6d)


 Click Next 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/faeb5549-25c5-418f-ab0e-1ec864ac6173)


Click on Standard Configuration 

Click Next 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/c31c84da-4c19-443f-8a0c-0636986ed804)

Click Next

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/1867178f-338e-45df-9782-10d37baf5f10)


Set password

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/5b173c7f-b914-4609-8a74-8ddee10fa293)


Click execute

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f8eca997-5a5c-48ab-9630-af8c608791e9)

Click Finish

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/a65bbbba-9d09-4eb5-af4e-f1c76befa40b)


Next we re going to do configurations inside of IIS

Go to remote Desktop and search for IIS, right click and run as administrator

Doubleclick on PHP Manager 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b80e70e6-7c82-44f8-bfea-d279a7074c1c)

Click on register new PHP 
Select ? 
Click Open 


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/45dc1891-f77f-4e00-a809-56ebedcd7ebc)

Install osTicket v1.15.8

   💡Download osTicket from the Installation Files Folder

   💡Extract and copy “upload” folder to c:\inetpub\wwwroot
 
   💡Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Once downloaded, open file 

Double click ![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/83757201-2cb7-493f-b03d-5941d4000f30)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/8a8bf1ce-6461-48d2-adce-4f831871a484)


Open additional file --- Drag upload folder to wwwrroot

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b1181189-fb01-4f1c-9401-1471f7759586)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b4b6c46a-3201-4f17-bfcb-7a904362989f)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/bd6c4530-4d9a-46dd-90fa-c74307833e0b)

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/d4d5a037-67ba-4154-8f2e-505bfd87dbf0)

Rename upload file to read osTicket

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/0cf8ef24-c2c4-4fa9-b821-cc42ae1a160e)

Let’s go back to IIS
Click on restart 
Go to sites -> Default -> osTicket
•	On the right, click “Browse *:80”

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/098bf229-5e62-49d0-9618-dc622254b292)


We have made it to osTicket! Congratulations! "👏

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/04edf95e-67ee-4055-a9a0-938cd9ec0a8f)

Note that some extensions are not enabled

   💡	Go back to IIS, sites -> Default -> osTicket
   
   💡	Double-click PHP Manager
   
   💡	Click “Enable or disable an extension”
   
   💡 Enable: php_imap.dll
   
   💡	Enable: php_intl.dll
   
   💡	Enable: php_opcache.dll
   
   💡	Refresh the osTicket site in your browse, observe the changes


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/9727892e-a80b-437b-b0f6-6823e4098eeb)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/a32a10e9-713e-4832-a33b-4fcddb6ff91a)


Refresh osTicket - Extensions should now been enabled

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/3af01bad-6f76-49a2-8fc6-f39bc951266c)


Rename: ost-config.php 

     '💡From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
     
	   '💡To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
    
![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/95fccffb-021c-4c30-aab1-8ecf22eb19dd)

Assign Permissions: ost-config.php

Disable inheritance -> Remove All

New Permissions -> Everyone -> All


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/10b7c87c-fbf2-422a-8479-a3e57c3dc9f4)


Continue Setting up osTicket in the browser (click Continue)

Name Helpdesk

Default email (receives email from customers)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/9f6f475d-1680-41f1-ba81-80704e95bf52)

From the Installation Files, download and install HeidiSQL.

💡Open Heidi SQL
💡Create a new session, root/Password1
💡Connect to the session
💡Create a database called “osTicket”


 ![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/03bf4534-299e-4538-b50d-2b7d7f3f03fa)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/7ce7c4a8-aff3-48ef-8a4d-84f3d97930bd)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/ec93d731-cf0a-44c5-845d-76dd74962d70)


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/e88d45b9-19fa-420b-8095-b12795096c94)

Continue setting up on the browser/filling out osTicket form

💡Enter MY SQL Username

💡Enter MySQL Password

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/8d9f44ac-5713-4239-817b-d09756f3c18c)

Go to Heidi and create a new database called osTicket

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/e4a30430-49bf-47d2-ae92-a83c4de58ab2)

Go back to browser and type in osTicket on the form where it reads mySQL Database: Click on Install Now 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/82c0c9f4-011a-4be9-b6e7-77edc3bd507d)

Completed osTicket

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b4b018a7-b212-4057-bf94-3639968330bf)
![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/9ed5f691-7502-4278-a0b6-e333dc95f3fa)


Congratulations! '🍾 osTicket has successfully been installed!! 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/4d88929d-022b-46c6-83a4-ea48f70d89f5)

Clean up time: 

    💡 Delete: C:\inetpub\wwwroot\osTicket\setup
   
    💡Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/a8ce14a5-f0e2-4276-8d6c-95cd8e8c4d61)


This concludes the demonstration. In the next tutorial, we are going to explore osTicket lifecycle. 



<p>
</p>
<p>

</p>
<br />
