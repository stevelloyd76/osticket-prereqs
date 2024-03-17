<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows Windows 10 (22H2)

<h2>List of Prerequisites</h2>

- Connect to your Virtual Machine with Remote Desktop
- Install / Enable IIS in Windows
- Install Web Platform Installer
- Install osTicket v1.15.8
- Download and Install HeidiSQL
- Created database for "osTicket
- Clean up 
- Change File Permissions

<h2>Installation Steps</h2>

<p>
  Installing all the necessary files is important to successfully installing the OsTicket Platform. We will use these files to install osTicket and some of its dependencies.


  ![84E92791-FF62-41C2-947B-1B424731A5EC_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/d9da9a56-9025-4620-80f9-a8d25b799551)

Install / Enable IIS in Windows WITH
CGI and Common HTTP Features
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
AND IIS Management Console
Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console

  ![BF77D07A-91E3-44A7-99DA-59F7F24B1784_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/23843ca9-c33e-4a84-8af6-97a76133a9d3)

  ![3CB8EE07-7997-4436-AA05-A1B956B30049_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/1b8395d0-0641-4aed-88b8-9f745f8e1617)

  ![91976F68-D06E-47CE-9744-AAA8D2CC0868_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/e9b5e09b-3f36-43da-a608-f9b5e0db6696)

<p>
Install / Enable IIS in Windows WITH
CGI and Common HTTP Features
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
AND IIS Management Console
Internet Information Services -> Web Management Tools -> IIS Management Console
	[X] IIS Management Console
</p>
<br />
Please follow the steps below to install osTicket v1.15.8:


1. Download and install VC_redist.x86.exe and MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the Installation Files.


2. Open IIS as an administrator and register PHP from within IIS.


3. Install osTicket v1.15.8 by downloading it from the Installation Files Folder, extracting and copying the "upload" folder to c: inetpub / wwwroot, and renaming it "osTicket" within c: inetpub / wwwroot.


4. Reload IIS (Open IIS, Stop and Start the server).


5. Go to sites -> Default -> osTicket and click "Browse *:80" on the right.


6. Note that some extensions are not enabled. To enable them, go back to IIS, sites -> Default -> osTicket. Double-click PHP Manager and click "Enable or disable an extension." Enable php_imap.dll, php_intl.dll, and php_opcache.dll.


7. Refresh the osTicket site in your browser and observe the changes.


8. Rename ost-sampleconfig.php to ost-config.php from C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php.


9. Assign permissions to ost-config.php by disabling inheritance, removing all permissions, and adding "Everyone" with "All" permissions.


10. Continue setting up osTicket in your browser by clicking "Continue," naming your helpdesk, and setting your default email to receive emails from customers.


11. Download and install HeidiSQL from the Installation Files.


12. Open HeidiSQL, create a new session with root/Password1 and connect to the session.


13. Create a database called "osTicket."


14. Continue setting up osTicket in your browser by entering "osTicket" for the MySQL Database, "root" for the MySQL Username, "Password1" for the MySQL Password, and clicking "Install Now!".


15. Congratulations, osTicket v1.15.8 should now be installed without errors!


<p>

  ![844D5F26-DEBE-462C-8982-AADFE4743840_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/24d884c8-4fcc-4ac7-87c1-b89cbe8dbe11)

_________________________
##OsTicket System:

Two Panels
- Admin Panel: Setting up the ticketing system settings, defining the roles and SLAs, and doing the administrative duties on a daily basis.

- Agent Panel: Generally using the platform for working 
tickets and helping users day to day.

- To add new users or customers to your account, access the Agent Panel and click the "Users" option. From there, select "Add New" and create a profile for each user, such as Karen or Ken.

  
  ![256C875F-F717-4BB2-9524-2A46BFDEE205_1_105_c](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/7f4166c7-c376-4ae7-9daa-34ded75c1496)


To configure roles, access the Admin Panel, click "Agents," then select "Roles." You can add or edit new roles, such as Supreme Admin, from there.

To configure departments, you can access the Admin Panel, click "Agents," then select "Departments." You can create or edit new departments, such as System Administrators.

To configure teams, access the Admin Panel, click "Agents," then select "Teams." From there, you can create or edit new teams, such as Level I Support and Level II Support.

To allow anyone to create tickets, you can access the Admin Panel, click "Settings," and then select "User Settings." Here, you can enable the option for registration and login to create tickets.

To configure agents, you can access the Admin Panel, click "Agents," and then select "Add New." From there, you can create new agent profiles, such as Jane and John.



  ![87B7824C-A538-4B54-881B-341E43FE8E61_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/de51ffc4-d0ec-4d29-95a3-76d00677edbb)


  ![3092EBA2-EA15-4C67-A5F3-065747A39C52_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/f72cf79a-500b-4abe-b0aa-3b0bc1a8421d)


User Client Portal Dashboard:
	- To open a new ticket, visit the help desk's client portal page. Once you have arrived at that page, click on one of the two “Open a New Ticket” buttons

  ![3BF22D5A-D74C-43BB-A0D5-DE40B3B0A828_1_201_a](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/40a70351-ee7c-4b27-9530-030651144aa1)


To manage your Service Level Agreement (SLA), access the Admin Panel and select "Manage," followed by "SLA." Here, you can set the priority levels for any issues that may arise, including Sev-A (1 hour, 24/7), Sev-B (4 hours, 24/7), and Sev-C (8 hours, business hours).

Additionally, you can configure your help topics by accessing the Admin Panel and choosing "Manage," followed by "Help Topics." You can add various topics, including Business Critical Outages, Personal Computer Issues, Equipment Requests, and Password Reset, to make it easier for your users to find the help they need.


  ![2D45CE17-15A5-4DBD-BED2-CD0F07446C00_1_105_c](https://github.com/stevelloyd76/osticket-prereqs/assets/162848869/11e5d32f-0ff1-4fac-82ad-d40145f28d10)


<p>
The Dashboard is meant to be a historical marker of the metadata in your help desk. It will give you an overview of tickets. The data can be filtered by date, departments, Help Topics, and Agents. It can also be exported into a CSV file.
</p>
<br />
