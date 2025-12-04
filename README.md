<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
A guide to installing a help desk ticketing system named osTicket.<br/>


<h2> Software & Technologies Used</h2>

- Windows 10 (Build 19044)
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)
- Internet Information Services (IIS)

  <h2> Prerequisites </h2>

- Create a Virtual Machine in Azure and install 
	- OsTicket v1.15.8
	- HeidiSQL
	- MySQL
	- PHP
	- Microsoft Visual C++ Redistributable
  
  <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>

<p>
<h3 align="center">First, start by creating a Resource Group inside Microsoft Azure! </h3>
<br />
</p>
<p>
	<img width="1440" height="661" alt="Screen Shot 2025-09-11 at 2 08 56 PM" src="https://github.com/user-attachments/assets/479c5d5d-9ef1-455f-8125-984e2bb3a1ee" />
</p>
<p>
<h3 align="center"> Now, create a Windows 10 Virtual Machine (VM). For username and password, they can be anything, but try to remember that this information will be used to access our main computer remotely. For the image, we will be using Windows 10, and for the size, it has to be at least 8 gigabytes. Lastly, when creating the Virtual Machine (VM) in Azure, remember to stay with the resource Group name you create to be organized.</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/dEF1c7h.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Open your Windows App on your computer and connect to your Virtual Machine that was created in Azure. </h3>
<br />
<p>
	<img width="1161" height="717" alt="Screen Shot 2025-09-29 at 1 20 34 PM" src="https://github.com/user-attachments/assets/87c94811-a2cb-459a-a1cf-eef5de0676f1" />
</p>
<h3 align="center">↓</h3>
<p>
	<img width="1163" height="711" alt="Screen Shot 2025-09-29 at 1 24 50 PM" src="https://github.com/user-attachments/assets/ed2e1ade-7464-4904-b49f-657ad0583f10" />
</p>
<br />
<br />
<h3 align="center">Now we need to install/enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).</h3>
<br />
<p>
	<img width="1137" height="768" alt="Screen Shot 2025-09-29 at 1 35 46 PM" src="https://github.com/user-attachments/assets/5766d46f-7ccd-472b-8232-47dcc236e5d5" />
</p>
<br />
<br />
<h3 align="center">Click to find "Internet Information Services" and expand it to be able to expand the "World Wide Web" tab. Afterward, expand the Application Developer tab to be able to click the "CGI" button and press ok. You will need CGI to download the PHP Manager.</h3>
<br />
<p>
  <img width="1440" height="900" alt="Screen Shot 2025-09-29 at 1 38 50 PM" src="https://github.com/user-attachments/assets/699cffbf-4fb5-4f47-8c72-8cdf2ceee64e" />
</p>
<br />
<h3 align="center">Install PHP Manager</h3>
<br />
<p>
<h3 align="center">Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.</h3>
<p>
	 <img width="1440" height="900" alt="Screen Shot 2025-09-29 at 1 41 17 PM" src="https://github.com/user-attachments/assets/4cab26dd-f596-4107-bcc6-38268fdf673d" />
</p>
<br/>
<h3 align="center">Install Rewrite Module</h3>
<br />
<p>
<h3 align="center">Download the Rewrite Module file, agree with all the terms, and it should now be installed onto the Computer. ৻(  •̀ ᗜ •́  ৻) </h3>
<p>
  <img width="1440" height="900" alt="Screen Shot 2025-09-29 at 1 42 41 PM" src="https://github.com/user-attachments/assets/f67a40e4-1200-4998-ba70-c7f165a55358" />
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> Open File Explorer, type "C:\" in the search bar. Right-click, and create a new folder called " PHP ".(The folder must be spelled exactly as you see it! (ᵕ—ᴗ—) ) Download php-7.3.8-nts-Win32-VC15-x86.zip from<a href="https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD"> Files You Need to Download</a></p>
<p>Extract it by going to where you downloaded the file, Right-click the PHP 7.3.8 file, and press extract to the PHP Folder you just created. ◝(ᵔᵕᵔ)◜
</p>
</h3>
<p>
  <img width="1440" height="900" alt="Screen Shot 2025-09-29 at 1 46 53 PM" src="https://github.com/user-attachments/assets/94b975cd-d7e6-40f5-a2a3-79c82e6d1359" />
</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, agree to the terms and conditions, and complete the installation process ദ്ദി(ᵔᗜᵔ)
</h3>
<p>
  <img width="1440" height="900" alt="Screen Shot 2025-09-29 at 1 48 37 PM" src="https://github.com/user-attachments/assets/adeb0224-f94a-4362-a97d-c5e937150938" />
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, accepting all terms and agreements until you reach the password section, where you will create a username and password for the database that will store the Ticket Information and be used in osTicket. (˶ᵔ ᵕ ᵔ˶)
</h3>
<p>
	 Username: root
</p>
<p>
	 Password: root
</p>
<p>
  <img width="1440" height="900" alt="Screen Shot 2025-09-29 at 1 49 19 PM" src="https://github.com/user-attachments/assets/48bb3bf1-7620-49fc-b090-f88e354fdfe6" />
<br/>
<h3 align="center">↓</h3>
  <img width="787" height="772" alt="Screen Shot 2025-09-29 at 1 51 27 PM" src="https://github.com/user-attachments/assets/0a8797e2-2d56-40ce-912b-938d4ec7ec84" />
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket
</p>
<p>
	Extract and copy the “upload” folder into c:\inetpub\wwwroot:
</p>
	<img width="786" height="788" alt="Screen Shot 2025-09-29 at 2 00 20 PM" src="https://github.com/user-attachments/assets/32434ed6-5173-40d6-af7d-39a584f1e79f" />
<p>
	<h3 align="center">↓</h3>
<p> 
	<img width="793" height="794" alt="Screen Shot 2025-09-29 at 2 06 03 PM" src="https://github.com/user-attachments/assets/e4332e91-4332-41d6-807b-b2070e9f27d5" />
</p>	
	Within c:\inetpub\wwwroot, rename “upload” to “osTicket”
</p>
<h3 align="center">↓</h3>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 08 20 PM" src="https://github.com/user-attachments/assets/35ef2565-f71e-466d-9c08-f6aa564e02b9" />
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server by right clicking "osticket-vm")</h3>
<br />
<p> 
	<img width="782" height="797" alt="Screen Shot 2025-09-29 at 2 10 42 PM" src="https://github.com/user-attachments/assets/9727d2be-3f62-410f-a746-a292f9b41b72" />
</p>
<h3 align="center">↓</h3>
<p> 
	<img width="785" height="796" alt="Screen Shot 2025-09-29 at 2 10 48 PM" src="https://github.com/user-attachments/assets/1e073bcb-803d-4426-b200-abec634fcc07" />
</p>
<p>
	Go to sites → Default → osTicket:
</p>
<p>
	<img width="795" height="789" alt="Screen Shot 2025-09-29 at 2 10 34 PM" src="https://github.com/user-attachments/assets/1422f331-976d-4a54-8610-3f46442a52d6" />

</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img width="794" height="797" alt="Screen Shot 2025-09-29 at 2 12 22 PM" src="https://github.com/user-attachments/assets/3d87d8e4-a060-4a1a-9294-eb14c1032fac" />
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites → Default → osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 15 45 PM" src="https://github.com/user-attachments/assets/447ea38b-21b3-4e3a-8b86-ca698020b0be" />
</p>
<p>
	Click “Enable”
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p> 
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 16 32 PM" src="https://github.com/user-attachments/assets/2ef8d4e8-686c-491a-9ae1-0d3bda4cdb5f" />
</p>	
<h3 align="center">↓</h3>
<p> 
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 16 52 PM" src="https://github.com/user-attachments/assets/622290d0-1226-420a-a9e9-b01d61577ac2" />
</p>	
<h3 align="center">↓</h3>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 17 11 PM" src="https://github.com/user-attachments/assets/5d834577-a24a-47f2-be11-c639278f0190" />
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 17 59 PM" src="https://github.com/user-attachments/assets/13c43211-4575-44d2-b52e-6baf930fcf0c" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 21 11 PM" src="https://github.com/user-attachments/assets/e064fe38-9d1c-43d7-8b5b-6d2570c7bd33" />
</p>
<h3 align="center">↓</h3>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 21 18 PM" src="https://github.com/user-attachments/assets/5db01426-c637-437f-a798-973d020105cf" />
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance → Remove All:
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 22 41 PM" src="https://github.com/user-attachments/assets/78581c88-3176-4788-8159-fca57bf85663" />
</p>
<p>
	New Permissions → Everyone → All:
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 24 10 PM" src="https://github.com/user-attachments/assets/0b6a7385-6058-4b3f-85ee-96ccb5ed68fb" />
</p>
<h3 align="center">↓</h3>
<p> 
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 23 41 PM" src="https://github.com/user-attachments/assets/eed51e1c-2fe0-43ae-a852-c9abf018b5c7" />
</p>
<h3 align="center">↓</h3>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 24 14 PM" src="https://github.com/user-attachments/assets/ab785342-44fd-41b7-bf74-6cc1a1dade1f" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Please name the helpdesk and enter your information as needed. Remember, the username and password will be used to log in to this account again, so please write them down or remember them (ㅅ´ ˘ `) 
</p>
<p>
	In this practice run, we aren't using real emails that work; however, in real-life scenarios, please use them ( •̯́ ₃ •̯̀) 
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 24 45 PM" src="https://github.com/user-attachments/assets/601eba6d-daad-4ca2-a82e-4098369ca227" />
<h3 align="center">↓</h3>
<p> 
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 27 08 PM" src="https://github.com/user-attachments/assets/5435d26c-8214-44cf-80ae-6e5cd2a28c7b" />
</p>
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 28 52 PM" src="https://github.com/user-attachments/assets/cf66dd4a-3df5-4109-a800-ee1aeb252319" />
<h3 align="center">↓</h3>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 29 16 PM" src="https://github.com/user-attachments/assets/f89438d2-b5af-4df6-86a8-b264009ca610" />
</p>
</p>
<p>
	Create a new session and connect to the session
<p>
	 Username: root
</p>
<p>
	 Password: root
</p>
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 30 58 PM" src="https://github.com/user-attachments/assets/4be225e9-9559-4363-a13b-91a52519a959" />

</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 32 24 PM" src="https://github.com/user-attachments/assets/de12effb-b653-4496-a307-9e478e0cf453" />

</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: root
</p>
<p>
	<img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 33 22 PM" src="https://github.com/user-attachments/assets/1a794347-df9f-4ff4-bd38-9145cda79225" />

	
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it's installed with no errors! Right? ∘ ∘ ∘ ( °ヮ° ) ?</hp>
<p>
	<img width="1435" height="714" alt="Screen Shot 2025-09-29 at 2 33 40 PM" src="https://github.com/user-attachments/assets/1fd5fe30-5444-4b45-b352-e5e13c4814b9" />

</p>
<br />
<h3 align="center">Login back into the osTicket Admin Panel </h3>
<br />
<p><img width="1440" height="900" alt="Screen Shot 2025-09-29 at 2 36 03 PM" src="https://github.com/user-attachments/assets/42ea2cf9-2a23-4ad5-a910-1b739666e380" />
</p>
<br />
<h3 align="center"> Congrats, you've finished installing osTicket! ദ്ദി(｡•̀ ,<)~✩‧₊ </h3>
