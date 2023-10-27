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

- Create a Resource Group in Azure
- Create a Virtual Machine (VM) in Azure
- Open Installation Files Link (holds downloads for installing)
  
Install various prerequisites '🖥️

    '💡 Install/Enable IIS in Windows
   
    '💡 Intall PHP Manager for IIS

    '💡 Install Rewrite Module

    '💡 Install PHP.7.3.8

    '💡Install MySQL 5.5.62

    '💡Install osTicket 

    '💡Install HeidiSQL

- Item 4
- Item 5

<h2>Installation Steps</h2>

We are going to Remote Desktop into newly created VM

Go to Azure and copy Public IP Address of VM 


    

Install/Enable IIS in Windows ( Internet Information Services)

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/05423c0e-d071-4529-8038-953ed7bf1265)

go to Google Drive where downloads have been saved

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/57ba7425-ca0c-4b67-a999-f1a6f7184d0d)

Install PHP Manager 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/aec0b5dd-191d-4cca-8d76-af26b67e516a)


Install Rewrite Module 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/ab837e60-5ce1-47b9-b5f2-9b2af97722f1)


Download PHP7.3.8 

Download and install VC redist

Download and install mySQL


![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/62e6d700-f50c-4b26-9383-10b6f1e8efd7)

Go to Start menu and type in: Remote Desktop 

Paste in IP address – Click Connect 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/5acf87ff-8ec3-47f4-924f-1d9895b8c7fe)


Click on Use a different account and enter credentials from your virtual machine in Azure

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f465fd23-a76d-41ee-bb89-27182c664600)
![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/5df66413-7e03-42bc-ae08-a3b20958a9fa)

Right Click on Start Menu
Type run: 


Click on Programs 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/99d0fd85-55bb-4d6e-abeb-27068b5737ac)

Click on Turn Windows features on or off

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/e50c71ea-e6db-4717-a2cd-2e12da5e17d8)

Install/Enable IIS in Windows ( Internet Information Services)

Install / Enable IIS in Windows WITH

CGI and Common HTTP Features

World Wide Web Services -> Application Development Features ->

[X] CGI

[X] Common HTTP Features


Search for Internet Information Services

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/7d040d18-985f-4e44-9902-10c3aa755b2b)

Click on the expand icon 

And then click on World Wide Web services

Under Application Development Features – Click on CGI

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b894c9aa-95bc-4748-bf29-fda1e498267b)


Under Common HTTP Features, make sure all the boxes are checked

Click OK

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/1738c350-c165-4b31-9496-a37d2ecf5802)

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/ebbfa26d-476f-42a2-a1f4-0e25b2e46f4f)

We are now going to check to see if IIS is installed. Go to a browser and type in 127.0.0.1

This page should appear 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/f42d97e1-04b6-4f70-95a9-dc2be73801d1)


Default IIS is now running 

Next we are going to download PHP Manager for IIS

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/b454153d-6ce4-49d0-975b-479264dab93e)

Click Next

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/163cab67-0420-4b9d-8d7c-72760536e660)




Click on I agree

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/ae2487ab-948c-44c6-92a6-f1b45077d9f5)


Installation is complete. Click Close 

![image](https://github.com/christyguajardo/osticket-prereqs/assets/147533626/cecbee98-0f9f-413d-895d-6b68e759d49f)

Install Rewrite Module: paste below in browser

Click download

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






<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
