


<br>
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
A tutorial outlining the prerequisites and installation of the open-source help desk ticketing system osTicket. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create a Resource Group in Azure portal
- Create Windows 10 Virtual Machine with 2-4 virtual CPUs


<h2>Executed Prerequisite Steps </h2>
  
<p>
<img width="912" alt="rglab1" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/f0f0afb1-7c70-4d29-a4c0-ffa019567737">

</p>
<p>
Create a Resource Group under your MS Azure subscripton. (The Region location typically should be based on your geographic location.)
</p>
<br />

<p>
<img width="903" alt="VM1 1" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/fac52778-f457-4c4f-9967-5c69ab5a5910">




</p>
<p>
Creating a VM Part 1: Create a Virtual Machine in the same region as your resource group (US East). Select your preferred OS for Image. We will be using Windows 10. 
</p>

<br />

<img width="878" alt="VM1 2" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/85f2051a-b5db-4908-acc4-cc7fb692ee35">

<br />

<br/>
Creating a VM Part 2: Select size of VM based on your business need. Create a username and password within requirments. Confirm hosting rights. Select Next:Disk > Next:Networking. 

<br/>

<br/>
<img width="945" alt="VM1 3" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/f74a004d-c4b4-41a2-b5d0-acde49a03331">

<br/>

<br/>
Creating a VM Part 3: Select Review + Create > Create to finalize the VM creation. 
<br/>
<br/>

<br />


<h2>List of Installation Steps</h2>

- (macOS) Install Remote Desktop and connect Virtual IP address
- Install and enable IIS 
- Install PHP Manager
- Install Rewritee Module
- Install VC redistributable
- Install MySQL
- Open IIS as an Admin.
- Register PHP
- Install Heidi SQL
- Install osTicket v1.15.8

  

<h2>Executed Installation Steps</h2>


<p>
  <br />
  
For Windows OS users, search "Remote Desktop" from the Start Menu. For macOS users, install Remote Desktop from App Store.
<b/>
<p>
  
  <img width="1075" alt="RD1 2" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/c92b231e-dfb2-4339-8d8b-bc73fca16f4d">
<p>

Connect Remote Desktop with your virtual IP address by selecting "add pc" on your Remote Desktop and copying your Virtual Machine's Public IP address in the Azure portal. Paste IP address in Remote Desktop under "computer" for Windows and "PC name" for Mac. Select Connect/Add. Create Username and Password. 
<p/>
<br />
<img width="1680" alt="Screenshot 2023-07-03 at 7 55 02 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/404f68d0-24c8-4925-b0a7-61802e03a1b5">


<p>
  
  Now we are connected to our Remote Windows Desktop under our Virtual Machine created through the MS Azure cloud. 
  Next we will need to configure IIS (Internet Information Services). You can configure ISS in your Remote Windows Desktop by going to Start Menu > Control Panel > Programs > click "Turn Windows features on or off" under Programs and Features > then select the box next to Internet Information Services. 
<br/>
<br/>

<img width="1113" alt="Screenshot 2023-07-03 at 7 39 22 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/cddbfd8e-10bb-475e-a82a-2fe14622e0b3">
<br/>
<br/> 
After seclecting Internet Information Services – click the + sign next to ISS to expand. Expand World Wide Web Services and then from there expand Application Development Features and select the box next to CGI. 
<br/>
<br/>


<p/>
<p>
<img width="1680" alt="Screenshot 2023-07-03 at 8 01 50 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/1ff96846-159c-4d08-bf5c-b95ce0a7ccb6">

</p>
<p>
Test by putting 127.0.0.1 into a web browser. The page shown above should load if all steps were executed correctly.


</p>
<br/>


<p>
<img width="1125" alt="Screenshot 2023-07-03 at 8 10 13 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/906e4164-bf68-42d7-9d3d-5497c8dccf26">

</p>
<p>
Install PHP Manager for IIS.
</p>
<br />

<p>
</p>
<img width="1123" alt="Screenshot 2023-07-03 at 8 19 10 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/84a9fcb7-d57f-4da4-af9f-63756adc92cd">

</p>
<p>
Install Rewrite Module.
</p>
<br />


<p>
</p>
<img width="1122" alt="Screenshot 2023-07-03 at 8 24 22 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/5f99b80c-1538-4d2e-b9d1-9d74a62f06cc">


</p>
<p>
<img width="1121" alt="Screenshot 2023-07-03 at 9 09 01 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/ffa995bd-77db-407c-9630-e3509ed9c086">
<br/>
Create a directory for PHP on your local hard drive (C:\PHP). Unzip downloaded PHP file into newly created PHP folder in the C drive. 
</p>
<br />



<p>
<img width="486" alt="Screenshot 2023-07-03 at 9 19 03 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/44f1a666-e7a7-46da-85ae-7c46ab37e282">

</p>
<p>
Install VC redistributable.
</p>
<br />

<p>
<img width="496" alt="Screenshot 2023-07-03 at 9 25 03 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/6d846221-7027-420a-b09a-fa1e1c60fd1d">
<img width="503" alt="Screenshot 2023-07-03 at 9 26 09 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/48342006-0608-426c-9afb-0c47cc83238e">

</p>
<p>
Install MySQL. Set credentials. 
</p>
<br />

<p>
<img width="775" alt="Screenshot 2023-07-03 at 9 32 25 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/af93c8cf-67b6-4a07-9889-97d35197db5c">

</p>
<p>
Open IIS as an Admin.
</p>
<br />

<p>
<img width="1243" alt="Screenshot 2023-07-03 at 9 43 34 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/e235f076-22d4-4a21-8d0d-9c23e00d54c7">

</p>
<p>
Register PHP from within IIS. Restart web server. 
</p>
<br />

<p>
  
<img width="1122" alt="Screenshot 2023-07-03 at 9 53 29 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/84622515-9291-404f-a392-6044b4f71af5">


</p>
<p>
Download osTicket and copy the "upload" file to C:\inetpub\wwwroot. Rename file to "osTicket" and restart server from IIS. 
</p>
<br />

<p>
<img width="1243" alt="Screenshot 2023-07-03 at 10 02 47 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/347eebbb-70ed-499b-9e62-490f2aef99e7">

</p>
<p>
From IIS select the server > Sites > Default Web Sites > osTicket. Select PHP Manager > enable or disable extentions and enable extensions. 
</p>
<br />

<p>
  
<img width="935" alt="Screenshot 2023-07-03 at 10 33 25 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/8a038127-dd68-42c2-8b27-e53a39045029">

</p>
<p>
Install Heidi SQL. Create a new Database in Heidi and name it osTicket. 
</p>
<br />


<p>
<img width="1225" alt="Screenshot 2023-07-03 at 11 01 06 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/cc76ee08-bb55-4de5-b6c0-c44596a38cc4">

</p>
<p>
Enter in the required credentials for installing osTicket and install. 
</p>
<br />


<p>
<img width="819" alt="Screenshot 2023-07-03 at 11 04 31 PM" src="https://github.com/technicallyjac/osticket_prereq-install/assets/138219436/e4699438-e74e-4516-b213-87e50047031a">

</p>
<p>
osTicket successfully installed.
</p>
<br />
