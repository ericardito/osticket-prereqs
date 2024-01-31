<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - The Installation Process</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket using.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop
- Internet Information Services (IIS)
<br />

<h2>Operating Systems Used </h2>

- Windows 10</b>
<br />

<h2>List of Prerequisites</h2>

- In Azure: Create a Resource Group & a Windows 10 Virtual Machine with 2 CPUs 
- Install & Enable IIS in Windows 
- Download & Install PHP Manager for IIS
- Download & Install URL Rewrite Module
- Download PHP 7.3.8
- Download & Install VCRedist
- Download & Install MySQL 5.5.62
- Download & Install Heidi SQL
- Install osTicket v1.15.8
<br />

<h2>Installation Steps</h2>
<p><h3> Create a resource group and virtual machine in Azure </h3></p>

<p><h3> Install / Enable IIS in Windows</h3></p>
<p>
<img src="https://i.imgur.com/xb0gIWq.png" height="50%" width="50%" alt="Turn Windows features on/off"/>
</p>
<p>
After you have created a Resource group and a Windows 10 VM in Azure, connect to Microsoft Remote Desktop (Mac users) with yourPublic IP/Login Info you created during its set up in Azure. </p>
<p>
In Windows, go to Control Panel > Programs > Programs & Features, and Turn Windows features on and off. 
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/Q2eQtEw.png" height="40%" width="40%" alt="Enable IIS"/>
</p>
<img src="https://i.imgur.com/Kiu5GQY.png" height="40%" width="40%" alt="Enable IIS"/>
<p>
Prior to the installation of osTicket, it is essential to have IIS, as osTicket is a web-based application. IIS (Internet Information Services) is the required software that enables your computer to host and showcase web pages on the internet.
<p>
Check "Internet Information Services" to enable it. After that, click on Web Management Tools > Application Development Features. Check CGI and Common Features to enable them as well.  
</p>
<br />


<p>
<p><h3>Install the PHP manager for IIS</h3></p>
<p>
<img src="https://i.imgur.com/APhG0WR.png" height="50%" width="50%" alt="Install PHP Manager for IIS"/>
</p>
<p>
Download and install PHP Manager for IIS. </p>
 <p>
PHP Manager for IIS is a tool that helps IIS work  with PHP. It makes sure that IIS can understand and process PHP code.
</p>
<br />
<br />



<p>
<p><h3>Install the rewrite module</h3>
</p>
<p>
<img src="https://i.imgur.com/b8dnEnN.png" height="50%" width="50%" alt="Install URL Rewrite Module"/>  
</p>
<p>
Download and install the URL Rewrite Module
</p>
<br />
<br />

<p>
<img width="235" alt="image" src="https://i.imgur.com/GvIvAsf.png">
</p>
<p>
On your Windows local disk C:\, create a folder and name it "PHP". Afterwards, Download PHP 7.3.8, and unzip its contents, by clicking "Extract all" into C:\PHP folder you've just created.  
</p>
<br />
<br />



<p>
<p><h3>Install VCRedist</h3>
</p>  
<p>
<img src="https://i.imgur.com/lCjQIfk.png" height="50%" width="50%" alt="Visual C++ instal"/>
</p>
<p>
Download and install VCRedist. </p>
<p>
</p>
<br />
<br />

<p>
<p><h3>INSTALL MySQL</h3>
</p>
<p>
<img src="https://i.imgur.com/5pnoFQi.png" height="50%" width="50%" alt="MySQL instal"/>
</p>
<p>
Download and install MySQL which gives osTicket a place to store information. </p>
<p>
 <p>
Choose "Typical Setup" and then choose "Standard Configuration".
 </p> 
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/dwrbxcp.png" height="50%" width="50%" alt="MySQL credentials"/>
</p>
<p>
The standard configuration sets you up with a "root" username. Add your own password and make sure it is one you can remember. You will need this later.
</p>
<br />
<br />


<p>
<p><h3>Open IIS and register PHP in IIS</h3>
</p>
<p>
<img src="https://i.imgur.com/NVoyTQW.png" height="50%" width="50%" alt="Open IIS as Admin"/>
</p>
<p>
Open IIS as an Admin. In the Windows search bar, write "IIS"
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/G79dbJV.png" height="50%" width="50%" alt="Register PHP within IIS"/>
</p>
<p>
In IIS, click on PHP Manager and then hit "Register new PHP version"
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/76uj5VK.jpg" height="50%" width="50%" alt="Pull CGI PHP folder"/>
</p>
<p>
You will be prompted to add a CGI with .exe extension. </p>
<p>
Select C:\PHP and you CGI file will appear. Click on it so IIS can register it.
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/Hss3BGE.png" height="50%" width="50%" alt="Reload IIS"/>
</p>
<p>
After making new additions it is always good to restart the server to ensure changes are made. Restart here and verify that the changes were made.
</p>
<br />
<br />


<p>
<p><h3>Install osTICKET</h3>
</p>

<p>
<img src="https://i.imgur.com/6t4JqBu.png" height="50%" width="50%" alt="Install OsTicket"/>
</p>
<p>
<p> Download and install osTicket. Then, move its "Upload" folder to your local disk C:\inetpub\wwwroot.
Within C:\inetpub|wwwroot, rename "Uplaod" to "osTicket"
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/q3xhHvs.png" height="50%" width="50%" alt="Reload IIS"/>
</p>
<p>
Restart the server once more
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/NuqfY0M.png" height="50%" width="50%" alt="Launch osTicket"/>
</p>
<p>
We are now ready to launch osTicket. On IIS, to your left click on "sites" > Default > osTicket. </p>
<p>
Then, to the right click "Browse *:80".
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/x3FhFLE.png" height="50%" width="50%" alt="osTicket missing extensions"/>
</p>
<p>
You are now in osTicket but note that some extensions are not enabled so next we will enable them.
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/KXD5swD.png" height="30%" width="30%" alt="Enabling .php extensions"/>
</p>
<p>
Go back to IIS, sites -> Default -> osTicket
</p>
Double-click PHP Manager
</p>
Click “Enable or disable an extension”
</p>
Enable: php_imap.dll
</p>
Enable: php_intl.dll
</p>
Enable: php_opcache.dll
</p>
Refresh the osTicket site in your browse, observe the changes
</p>
<p>
</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/YNcH6PR.png" height="40%" width="40%" alt="Enabling .php extensions"/>
</p>
<p>
<br />
<br />


<p>
<p><h3> Rename "ost-sample config" file and assign new permissions to "ost-config" file</h3>
</p>
<p>
<img src="https://i.imgur.com/HoZsoRH.jpg" height="40%" width="40%" alt="Rename ost-sampleconfig to ost-config"/>
</p>
<p>
</p>
<p>
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
 </p>
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />
<br />



<p>
<img src="https://i.imgur.com/dlq2GZ8.png" height="40%" width="40%" alt="Assign Permissions of ost-config.php"/>
</p>
<p>
Assign new permissions to our ost-config.php file we have just renamed. </p>
<p>
Properties > Security > Advanced
 </p>
Disable inheritance -> Remove All
</p>
New Permissions -> Everyone -> All
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/T1VykEH.png" height="40%" width="40%" alt="Assign Permissioms of ost-config.php"/>
</p>
<p>
</p>
<br />
<br />

<p>
<img src="https://i.imgur.com/9ZV9AD9.png" height="40%" width="40%" alt="Give full control to Everyone"/>
</p>
<p>
Give full control to the group "Everyone"
</p>
<br />
<br />


<p>
<p><h3>Setting up osticket in the browser</h3>
</p>
<p>
<img src="https://i.imgur.com/a1AOVHG.jpg" height="40%" width="40%" alt="Setting up osTicket in the browser"/>
</p>
<p>
Go to osticket in your browser, click "Continue". You may now fill out the.
<p>
Once you have filled out the forms, do not press the install button yet.
</p>
<br />
<br />


<p>
<p><h3> Install HeidiSQL</h3>
</p>
<p>
<img src="https://i.imgur.com/tQs84VR.png" height="40%" width="40%" alt="Download and Install Heidi SQL"/>
</p>
<p>
Download and install Heidi SQL
</p>
<br />
<br />


<p>
<p><h3>Create a new session in HeidiSQL</h3>
</p>
<p>
<img src="https://i.imgur.com/dKQA9vu.png" height="40%" width="40%" alt="Create a new session Heidi"/>
</p>
<p>
Open Heidi SQL
 </p>
Create a new session, root/Password1
</p>
Connect to the session
</p>
Create a database called “osTicket”
</p>
<br />
<br />
<p>
<img src="https://i.imgur.com/5vQTFjA.png" height="40%" width="40%" alt="Create a database in Heidi"/>
</p>
<p>
</p>
<br />
<br />



<p>
<p><h3>Finish setting up and installing osTicket in the browser</h3>
</p>
<p>
<img src="https://i.imgur.com/Nv2821N.png" height="40%" width="40%" alt="Continuing osTicket set up"/>
</p>
<p>
You may now fill out the remaining fields in the browser for osTicket and then hit "install now"
</p>
<br />
<br />

<p>
<p><h3>Congratulations, hopefully it is installed with no errors!</h3>
</p>
<p>
<img src="https://i.imgur.com/vGGvrXI.png" height="40%" width="40%" alt="Congrats, you're in!"/>
</p>
<p>
<h4>
</p>
<p>
<p><h3>Clean up</h3>
<p>Delete: C:\inetpub\wwwroot\osTicket\setup </p>
<p>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php</p>
<br />
<br />


<p>
<img src="https://i.imgur.com/mVPaq3y.png" height="50%" width="50%" alt="osTicket help desk page"/>
</p>
<p>
<h4> Help Desk Login Page - http://localhost/osTicket/scp/login.php </h4>
</p>
<h4>End Users osTicket URL: http://localhost/osTicket/ </h4>
<br />
<br />
