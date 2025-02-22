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

![image](https://github.com/user-attachments/assets/6932b7f4-6db0-4624-b471-74a212c21130)




 
</p>
<br />
