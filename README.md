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
 <img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/98524ac3-5b2b-426d-a1ed-ce40ba4396a9"
</p>
<p>
Step 1: From the home page click on Resouce Groups. You should be in the resource groups tab. Now you need to click (Create new resource group). Under Subscription there should be a blank space to name youre group. Name it (RG-osTicket). And in the Region tab under it put (US West 3) because some reason when you put another region it doesnt show up in youre resource groups. After that you should be set for the resource group now click (Review + Create)
</p>
<br />

<p>
<img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/b5102b98-8602-4c89-8af9-44baa70c8b3b"
"/>
</p>
<p>
Step 2: Go back to the home page and head to the Virtual Machines tab. Once you are there click Create in the upper left corner. Then click Azure Virtual Machine. Under subcription you want to make the resource group the one you just made which is (RG-osTicket). There should be a option. Youre Virtual Machine name will be (VM-osTicket). Region will stay (US West 3) Security Type change to Standard. Image (Windows 10 Pro, version 21H2) For size minumum should be (2 vcpu 16 GiB memory). Username is Labuser then create your own password. When youre finished check the "I confirm" box at the bottom and then Review + Create.
</p>
<br />

<p>
<img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/3096cf06-f613-4db2-bdd2-5b7a8bfd4c1b"
"/>
</p>
<p>
Step 3: Go To Virtual Machines Tab and click the VM you just created. Copy the Public IP address and in youre search tab for windows at the bottom left corner search (Remote Desktop). After you click on it paste the IP and log in with the User and Pass you made in Step 2. When logged into the VM go to Internet Explorer and plug in this link( https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 ).
</p>
<br />

<p>
<img
</p>
<p>
<h2>Download Section</h2>
 
 First you want to open contol panel in the VM. Then go to programs. Under programs and features you want to click (Turn Windows features on or off). Scroll untill you find (Internet Installation Services) Check and expand the box and expand (World Wide Web Services and Application Development Features) Enable CGI and in Common HTTP Features check all the boxes.
 
 <img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/210700ab-cfdb-4954-bd71-944f3d80c8f0"/>

 Next you want to Download and Install PHP Manager from the Google Drive link. Then Download and Install the (Rewrite Module) also. Next open file explorer and go to your C drive and you are going to make a new folder named (PHP). Go back to the Google Drive downloads and download ( https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=drive_link ) and if you get a message click download anyway and keep the file. Go back to file manager and go to the downloads folder and youre going to right click the download and Extract All to the (PHP)folder you made in the C Drive.
 
<img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/49fcf19f-ee70-4300-898a-aa0880ca9b7a"/>

 
 Next download and install (VC_Redlist) in the Google Drive link. After that download (Mysql-5.5.62) In the Install window you want to make a (Typical) account then your going to setup your credintials after the install. First your going to change the configuration from Detailed to Standard. From there create a password and dont forget. Youre username will be (root).Execute the install. It should look like this when finished.

<img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/59659562-bbab-4c7a-bb2a-dfba76d68436"/>
"/>
 
 Then in the Windows start search (iis) right click it and open as a admin. In IIS open PHP Manager and Register a new PHP version. Browse by clcking the three dots in the tab and open the PHP Folder you made in the C Drive and click (php-cgi) and open. And back in the IIS Tab restart the web server by clicking restart on the right side under actions. 
 
<img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/39e16742-734c-421d-8302-366d2cc36c34"/>


 Lastly download osTicket from the Google Drive link. Open download folder in file explorer and click the osTicket download then open another file explorer tab and youre going to drag the upload folder into the (wwwroot) folder. To get there in the other file explorer tab go to the C drive and then (inetpub) and click (wwwroot) then drag the upload folder from the osTicket download. After its finished transfering right click the upload folder and rename it to osTicket. Go back to IIS and (Stop and Restart) in the Actions tab on the right. 
 
<img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/26618407-4009-4c6a-b8f0-d13167a024f1" />

 
 Next go to sites in connections on the left and Default Web Site then click osTicket. Then on the right under Manage Folder click (Browse *80) And osTicket should load. Go back to IIS one more time and click (PHP Manager) in the osTicket folder. At the bottom in PHP Extensions click enable or disable a extension. And youre going to enable php_imap.dll, php_intl.dll, and php_opcache.dll. and refresh the tab that you have osTicket in. 
 
 <img src="https://github.com/CoreyJeff/osticket-prereqs/assets/138095936/69a4ec62-75e1-46ce-8044-479a9c33d94b"/>

 
 Open file explorer and go back to the (wwwroot) folder and click osTicket then (Include) and scroll until you find                      
 (ost-sampleconfig.php)Rename this to (ost-config.php). Right click and go to properties and then security. At the bottom of Security click advanced and disable inheiritance. You will get a popup and select Remove all permissions from this object. After this your going to click add to add permissions and select a principal. in the blank box type (everyone) Check Names and press OK. Then click Full control and Apply. Now we are going to setup osTicket in the browser. The System Settings and Admin User sections you can personalize yourself. But for the Database Settings section you are going to need to download and install (HeidiSQL) in the Google Drive link. Open HeidiSQL and create a new connection at the bottom left corner. Remember yore username is (root) and whatevr you made your password. Then simply click open and you should have a connection. Now you want to right click Unnamed and create new and name it osTicket. Back in the osTicket browser in Database settings under (MySQL Database) you want to name it osTicket. Lastly press Install Now and it should install osTicket. And for cleanup you need to open file explorer again and go to C:\inetpub\wwwroot\osTicket and delete the setup folder. While youre in the file explorer still go to C:\inetpub\wwwroot\osTicket\include and right click ost-config.php go to properties then security and advanced and edit from Full Control to just Read & Execute and Read. Admin URL  ( http://localhost/osTicket/scp/login.php ) Creating Tickets URL  ( http://localhost/osTicket/ ) 


