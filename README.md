# osticket-prereqs

<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure for Virtual Machines/Computer (Optional)
- Remote Desktop (Optional)
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Resource Downloads</h2>

- osticket setup folder download: https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0

<h2>Installation Steps</h2>

<p>
1. Download the osTicket setup folder from the link above and unzip it onto your desktop. The extracted folder should be called "osTicket-Installation-Files" We will be using all the files in this folder to install osTicket. You may delete the zipped folder after the extraction is complete. 
</p>
<br />
<p>

![image](https://github.com/user-attachments/assets/d22898e2-30ca-4984-8a47-facd9e913fee)
![image](https://github.com/user-attachments/assets/4e0a86b5-c8d6-45c1-a82f-8a97ff074f43)

</p>

<br />

<p>
</p>
<p>
  
2. Open the Windows control panel then navigate to Programs>Turn Windows features on and off then scroll down and select "Internet Information Services" and press OK to install it. This step allows us to create a web server that accepts requests from remote clients and returns appropriate responses.
<br />
  
</p>


![image](https://github.com/user-attachments/assets/d146418e-f4f7-4b2b-ab2c-430e6266cd83)
![image](https://github.com/user-attachments/assets/f29daf8e-a100-401f-868e-4d7d7f216a2e)
![image](https://github.com/user-attachments/assets/2b979efa-7d8b-4d90-b4e7-765dc7ca16b7)
![image](https://github.com/user-attachments/assets/3917cac3-35d4-4993-be1c-2f446f80a5b0)





<br />

<p>

</p>
<p>
3. From the “osTicket-Installation-Files” folder, install:
  
  - PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
  - Rewrite Module (rewrite_amd64_en-US.msi)
  - VC_redist.x86.exe
<b />

![image](https://github.com/user-attachments/assets/79e91709-7770-4112-a0fc-8e06f1495766)





 
</p>
<br />

<p>
  
4. Create a folder on your C drive and name it "PHP" and place all the files from the unzipped PHP 7.3.8 folder into it. 
  
<br />  


![image](https://github.com/user-attachments/assets/32e2a413-a3cd-47f9-9008-dffea6a73aa7)
![image](https://github.com/user-attachments/assets/eefb9d41-2f9c-489c-921b-709b6ba8d537)

</p>
<br />

<p>

  
5. Create a folder on your C drive and name it "PHP" and place all the files from the unzipped PHP 7.3.8 folder into it. 
  
<br />  
<b />

![image](https://github.com/user-attachments/assets/32e2a413-a3cd-47f9-9008-dffea6a73aa7)
![image](https://github.com/user-attachments/assets/eefb9d41-2f9c-489c-921b-709b6ba8d537)

</p>
<br />

<p>

  
6. From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
   
  - Typical Setup ->
  - Launch Configuration Wizard (after install) ->
  - Standard Configuration ->
  - Username: root
  - Password: root


   
  
<br />  
<b />

![image](https://github.com/user-attachments/assets/b6e93092-bc57-4940-b956-85c63bf78034)
![image](https://github.com/user-attachments/assets/fc5b6311-dffc-42d9-8567-81bdaaa2a334)


</p>
<br />

<p>

  
7. Open IIS as an Admin

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

Reload IIS (Open IIS, Stop and Start the server)



   
  
<br />  
<b />

![image](https://github.com/user-attachments/assets/1166c8e0-fc4d-4641-8224-1eb9c518789f)
![image](https://github.com/user-attachments/assets/19402f07-2d00-417d-8305-2ce4e9984fd0)
![image](https://github.com/user-attachments/assets/1314c875-6d50-439a-aa51-f439442a0513)
![image](https://github.com/user-attachments/assets/f5fa653c-3519-4a80-aa31-0f5f2bb467cb)

</p>
<br />

<p>

  
8. Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
Then reload IIS (restart server same as the previous step)



   
  
<br />  
<b />

![image](https://github.com/user-attachments/assets/0516b72e-4b5f-47ef-88d3-f8b72e016eb9)
![image](https://github.com/user-attachments/assets/e52eacdc-8194-4433-8bd4-95ca9711c90e)
![image](https://github.com/user-attachments/assets/468e1b7b-5d59-4d4b-baac-f14249e578bc)

</p>
<br />

<p>

  
9. Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll

<br />  
<b />

![image](https://github.com/user-attachments/assets/74ad3448-0cc3-45e2-bf14-945684aecc69)
![image](https://github.com/user-attachments/assets/e016a810-e4ae-4077-911a-3ee87cac780d)
![image](https://github.com/user-attachments/assets/b44cd324-c042-43ea-9e55-89e996b9c71c)
![image](https://github.com/user-attachments/assets/ea553ee7-94c7-4d9d-83bf-d2cd90c57eaa)

</p>
<br />

<p>

  
10. Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Right click and open properties
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

This will make osTicket able to fully control our new configuration files.
  
<br />  
<b />

![image](https://github.com/user-attachments/assets/af422fbe-2018-49ea-992d-472212ff359d)
![image](https://github.com/user-attachments/assets/e73c7d55-8239-4070-958e-25be798cfb18)
![image](https://github.com/user-attachments/assets/9f57845d-35fc-412f-8d8e-ae3e7a52a822)
![image](https://github.com/user-attachments/assets/98a5c938-d7c1-410e-953a-ea04997ff54e)
![image](https://github.com/user-attachments/assets/3630b517-2f56-4773-9ebe-4bfe40d0f0f7)
![image](https://github.com/user-attachments/assets/a1e3b39a-b6a7-4a8e-8761-e57b9b4c3d67)
![image](https://github.com/user-attachments/assets/259e7420-c149-43b6-93cd-1d3a7886bb4a)

</p>
<br />

<p>

  
10. Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
You can use fake emails

From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
  
<br />  
<b />

![image](https://github.com/user-attachments/assets/e6f89ef5-36f8-4676-a4f8-85f375a958af)
![image](https://github.com/user-attachments/assets/0dac9fb5-ae28-4900-8681-408e367f6e13)
![image](https://github.com/user-attachments/assets/5bab4a71-0412-4368-95c3-1c0391133b63)
![image](https://github.com/user-attachments/assets/f98b4e5d-7707-49af-af15-2781c99261fe)
![image](https://github.com/user-attachments/assets/8c6b3bd4-2846-4935-b69b-ee93f8344bd8)
![image](https://github.com/user-attachments/assets/b5a3f6db-d669-4fa7-ab38-355af836604e)

</p>
<br />

<p>

  
11. Finish! Hopefully, osTicket is installed correctly with no errors!
  
<br />  
<b />

</p>
<br />




