<p align="center">
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

- Step 1: Create A Resource Group In Microsoft Azure
- Step 2: Add Vitual Network And Subnet To The Resource Group
- Step 3: Install osTicket On The Virtual Machine


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 1: From the home page click on Resouce Groups. You should be in the resource groups tab. Now you need to click (Create new resource group). Under Subscription there should be a blank space to name youre group. Name it (RG-osTicket). And in the Region tab under it put (US West 3) because some reason when you put another region it doesnt show up in youre resource groups. After that you should be set for the resource group now click (Review + Create)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Go back to the home page and head to the Virtual Machines tab. Once you are there click Create in the upper left corner. Then click Azure Virtual Machine. Under subcription you want to make the resource group the one you just made which is (RG-osTicket). There should be a option. Youre Virtual Machine name will be (VM-osTicket). Region will stay (US West 3) Security Type change to Standard. Image (Windows 10 Pro, version 21H2) For size minumum should be (2 vcpu 16 GiB memory). Username is Labuser then create your own password. When youre finished check the box at the bottom and then Review + Create.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Go To Virtual Machines Tab and click the VM you just created. Copy the Public IP address and in youre search tab for windows at the bottom right corner search (Remote Desktop). After you click on it paste the IP and log in with the User and Pass you made in Step 2. When logged into the VM go to Internet Explorer and plug in this link( https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 ).
</p>
<br />

<p>
<img
</p>
<p>
Download Section
