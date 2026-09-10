# osTicket-Prerequisites and Installation steps
# Description
This tutorial outlines the prerequisites and installation steps of the open source help desk ticketing system, osTicket
# Environments and Technologies Used
- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (IIS)
# Operating Systems Used
- Windows 10
# Prerequisites Needed
- Microsoft Azure
- Virtual Machine
- osTicket Installation Files
# Installation Steps
# Step 1: Connect to your Virtual Machine with Remote Desktop
<img width="2234" height="1212" alt="image" src="https://github.com/user-attachments/assets/bf7c7bc9-fc41-4673-a1f7-092c8bbe84dc" />

After your VM engine has started, if using a Mac you will need to open up a session on the windows app using the Public IP address from your VM. Using the credentials saved, you will be able to open up a remote desktop session.
<img width="2234" height="1212" alt="image" src="https://github.com/user-attachments/assets/73fd4c09-5ffe-4c6a-88aa-dec9abd9593c" />

# Step 2: Install and Enable Internet Information Services (IIS) in Windows

- At the bottom left, search for Control Panel
- Underneath Programs, select Uninstall a Program
- On the left side of the screen, select Turn Windows Features On or Off
- Select Internet Information Services (IIS), and select OK
<img width="855" height="541" alt="image" src="https://github.com/user-attachments/assets/406e9aa2-e2bd-465b-95e7-dd7209884646" />

# Step 3: Download, Install, and Open the Web Platform Installer

- Download Web Platform Installer > select Download Anyway > at the top right, select Open File
- Follow the prompt to install Web Platform Installer
- Open the Web Platform Installer
<img width="3360" height="2100" alt="image" src="https://github.com/user-attachments/assets/44e8c690-7004-4ef7-91c9-f0a81f7259c8" />
<img width="3360" height="2100" alt="image" src="https://github.com/user-attachments/assets/c42c77cd-50a3-4fce-ae9a-c79bc4ac7a4d" />

- With Web Platform Installer open, go to top right of the screen and search for MySQL 5.5
- Go to MySQL Windows 5.5 and click Add
- Go to the top right again and search for PHP
- Add all simple versions of x86 PHP up until 7.3
- Select Install at the bottom of the screen and it will tell you to create a username and password to complete the installation
<img width="3360" height="2100" alt="image" src="https://github.com/user-attachments/assets/bfa70ff4-1551-46db-abe7-e5b3a4e2d936" />
<img width="3360" height="2100" alt="image" src="https://github.com/user-attachments/assets/8e35e66b-7dcb-4662-8df0-de3b88a8cefe" />

- Username: root
- Password: Password1
- Follow the prompt to finish installing
- You should get a message stating that "some products have failed to install", ignore and finish
- Download and install the following from within the lab files
- PHP Version 7.3.8
- PHP Manager 1.5.0 for IIS 10
- Microsoft Visual C++ 2009 Redistributable Package
<img width="1374" height="948" alt="image" src="https://github.com/user-attachments/assets/94d17c1e-c51a-4c66-8ec8-9f8bd46a2283" />
<img width="3360" height="2100" alt="image" src="https://github.com/user-attachments/assets/b655f9fa-f371-41b7-8dcf-b668eaac8caa" />

# Step 4: Install osTicket v1.15.8

- Download osTicket (download from within lab files)
- Right-click on the file and select Extract All
- Open the new osTicket folder
- Copy the Upload folder into C:\inetpub\wwwroot
- Rename “Upload” to “osTicket”
<img width="2224" height="1252" alt="image" src="https://github.com/user-attachments/assets/c677a359-2286-4004-a5a2-ba1086d9696c" />
<img width="2260" height="1158" alt="image" src="https://github.com/user-attachments/assets/b65b6db5-9c67-4f93-8666-3ec272c57cd9" />

# Step 5: Restart the IIS Server

- Search for Internet Information Services (IIS) and select Open
- Click on restart on the right side of the page
- On the left side of the screen, click Virtualmachine > Sites > Default Website > osTicket
- On the right side of the screen, click “Browse *:80”
- osTicket should open up in your browser
- Before you continue, head back to IIS
- Open IIS
<img width="1079" height="546" alt="image" src="https://github.com/user-attachments/assets/7856d8ed-d62c-46bb-9aad-b0891d5a5bf0" />
<img width="1079" height="625" alt="image" src="https://github.com/user-attachments/assets/18580901-34ce-4e31-b495-26ed5d8570dc" />

# Step 6: Enable Extensions in IIS

- Go back to IIS > Sites > Default Web Site > osTicket
- Double-click PHP Manager
- Click “Enable or Disable an Extension” at the bottom of the screen under PHP Extensions
- Right-click and enable the following
  - php_imap.dll 
  - php_intl.dll
  - php_opcache.dll
