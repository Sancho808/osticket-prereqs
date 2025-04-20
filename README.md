# osticke<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>


<h1> How to Install osTicket </h1>
This is an easy guide to installing a help desk ticketing system called osTicket.<br/>


<h2> Files You Need to Download</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfdaNfdZsUwxWYChf6) 📁
<h2> Software & Technologies  Used</h2>

- Windows 10 (Build 19044)
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)
- Internet Information Services (IIS)

  
    <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />                                                                                                                                                        
                                                                                                                   
 Create a Resource Group inside Azure.                                                                                                                                 
                                                                                                                   
                                                                                                                   
![image](https://github.com/user-attachments/assets/dd3825a7-fcd9-4654-9d35-5760e96707fb)
                                                                                                                                                                                                                                                                                                                                                         
                                                                                                               
                                                                                                               
                                                                                                             
Create a Windows 10 Virtual Machine (VM), typically with 2-4 Virtual CPUs. For username and password, it can be anything. This will help with the overall speed of the VM.                                                                                                                                                                                                                                                                                                                                                     
                                                                                                            
![image](https://github.com/user-attachments/assets/d1285e52-47ef-4f6f-92f6-8c221185718c)
![image](https://github.com/user-attachments/assets/74d29ea4-46fd-483f-88af-3ea8d936e65c)
![image](https://github.com/user-attachments/assets/5f2f8b75-919f-49fa-be37-f48eb91c2262)
<h3 align="center">Remote Desktop Connection</h3>                                                                                                                                         
<p>Now to, Remotely to connect the VM using Remote Desktop Protocol. Next using the IP address from the Windows VM, copy it into the RDP software, use the same name you logged in with the username & password you would have used when you created the VM.                                                                                                                                                                                                                                          
                                                                                                                   
 ![image](https://github.com/user-attachments/assets/41e54d3d-41f1-4707-b18f-abeb73bd6f52)
                                                                                                                                                                                                                                                                                                                                                
                                                                                                          
                                                                                                      
Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.                                                                                                       
                                                                                                                                                                                                                                                                                                                                        
 ![image](https://github.com/user-attachments/assets/69bd0998-4277-4c88-83dc-925e28b32631)
                                                                                                                                                             
  </p>                                                                                                                                                                                 
  <br>                                                                                                                                                                                         
<h3 align="center">Install PHP Manager</h3>

 <h3 align="center">Download the PHP manager file, and agree with all the terms. Now PHP manager is downloaded to our operating system.</h3>
<p>                                                                                                                                     
                                                                                                                                                       
                                                                                                                                                                    
                                                                                                                                                                    
 ![image](https://github.com/user-attachments/assets/0d777fcb-e7b4-4ab8-9c6a-a87640fa45e5)
                                                             
   <h3 align="center">Install Rewrite Module</h3>                                                                                                                                                             
  <br />
<p>
<h3 align="center">Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.</h3>
<p>                                                                                                                                                                                        
                                                                                                                                                                                          
![image](https://github.com/user-attachments/assets/f6d5a4a1-eb7a-44c0-a736-7a15ab8d7253)
                                                                                                                                                                   
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>                                            
<h3 align="center"> Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from<a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> Files You Need to Download</a>, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.
</h3>
<p>                                                                                                                                                                                       
                                                                                                                                                                                          
 ![image](https://github.com/user-attachments/assets/aff31b37-f23f-44a6-b85c-1b582bad8bec)

</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, Agree with any terms and agreements and finish installing.
</h3>
<p>                                                                                                                                                                                      
                                                                                                                                                                                         
![image](https://github.com/user-attachments/assets/d6923514-6776-4731-9437-fa170cc531ca)
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>                                                                                                                                                                                      
                                                                                                                                                                                         
 ![image](https://github.com/user-attachments/assets/afc5c227-9abe-4e22-84ee-8932a2ba388f)
                                                                                                                                                                                                        
                                                                                                                                                                                                         
          

</p>![image](https://github.com/user-attachments/assets/c347b14b-cdb5-4d19-a067-18af718f339b)

<br />

<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:. Inside C:\inetpub\www.root rename upload to osTicket. Load IIS again and stop & restart server. Then goto sites-> default-> osTicket. Browse folder and click Browse *;80(HTTP) 
</p>                                                                                                                                                                                                      
<p>                                                                                                                                                                                                  
                                                                                                                                                                                                         
![image](https://github.com/user-attachments/assets/06915130-e228-4fa4-8866-f7aab42608ca)
 ![image](https://github.com/user-attachments/assets/18c546c4-13f7-423c-a8f0-44b344cc4286)
![image](https://github.com/user-attachments/assets/e9440d79-021d-4297-8d7f-029e0f12654d)
![image](https://github.com/user-attachments/assets/12932447-3cc1-41da-bd1f-9f508bde5fd6)
</p>
<p> Now goto sites-> default-> osTicket. Double click PHP Manager Extensions= able or disable= enable php_imap.dill/php_inti.dill/php_opcache.dill refresh server.                                                                
</p> 
<p>                                                                                                                                                                                                      
                                                                                                                                                                                                         
 ![image](https://github.com/user-attachments/assets/ad680cd6-1251-4ae1-89fc-25fb7c6d938c)
 ![image](https://github.com/user-attachments/assets/ead0ca0f-6ed4-4473-be0d-2150c2f13aee)
                                                                                                                                                                                                                                                                                                                                                                                                             
 </p>                                                                                                                                                                                                 
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p></p>
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
<br />t-prereqs
