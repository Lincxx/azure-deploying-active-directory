#  Deploying Active Directory
---
In this lab we are going to install AD and create a new forest. 
From we are going to setup an Organizational Unit (OU) called "_EMPLOYEES" and "_Admins"
---

## Part 1
### Install Active Directory
—
### Login to DC-1 and install Active Directory Domain Services
![step1](https://github.com/user-attachments/assets/7a6b613f-2224-4db2-b4bd-ff9f9141c71e)

![step2](https://github.com/user-attachments/assets/587c653a-f892-44a3-b310-5d17fda28f0d)

![step3](https://github.com/user-attachments/assets/0d2ce55b-93e0-4292-8d5b-353f03491f2e)

![step4](https://github.com/user-attachments/assets/00ae2f55-8d56-4f0a-84d7-142b1ebdd4ac)

![step5](https://github.com/user-attachments/assets/f3ac00b1-8044-42cd-b62e-4cfc50552360)

![step6](https://github.com/user-attachments/assets/f840f029-6107-40c1-a2dd-7b342905d37a)

![step7](https://github.com/user-attachments/assets/52efddf1-bd31-4664-b9ca-40329f73c32c)

![step8](https://github.com/user-attachments/assets/1379b497-c0b4-416d-8989-6ffae22e043c)

![step9](https://github.com/user-attachments/assets/b7349ad3-9e9a-45fa-9e38-ff954ed65e16)

![step10](https://github.com/user-attachments/assets/94456de6-c918-49f6-b70d-92badcd59a3d)

![step11](https://github.com/user-attachments/assets/22906f29-4d07-432d-b107-65fa7d48eda9)

### Promote as a DC: Setup a new forest as mydomain.com (can be anything, just remember what it is)
### Restart and then log back into DC-1 as user: mydomain.com\labuser

### Create a Domain Admin user within the domain
—
### In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”
### Create a new OU named “_ADMINS”
### Create a new employee named “Jane Doe” (same password) with the username of “jane_admin” / Cyberlab123!
#### Add jane_admin to the “Domain Admins” Security Group
### Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”
### User jane_admin as your admin account from now on


### Join Client-1 to your domain (mydomain.com)
—
From the Azure Portal, set Client-1’s DNS settings to the DC’s Private IP address (Already done)
From the Azure Portal, restart Client-1 (Already done)
Login to Client-1 as the original local admin (labuser) and join it to the domain (computer will restart)
Login to the Domain Controller and verify Client-1 shows up in ADUC
Create a new OU named “_CLIENTS” and drag Client-1 into there

Finish the lab, but do not delete the VMs in Azure. We will use them for upcoming labs.
If you are done for the day and want to save money, simply “Stop”/turn off the VMs within the Azure Portal

Part 2

Turn on the DC-1 and Client-1 VMs in the Azure Portal if they are off.
Setup Remote Desktop for non-administrative users on Client-1
—
Log into Client-1 as mydomain.com\jane_admin
Open system properties
Click “Remote Desktop”
Allow “domain users” access to remote desktop
You can now log into Client-1 as a normal, non-administrative user now
Normally you’d want to do this with Group Policy that allows you to change MANY systems at once (maybe a future lab)


Create a bunch of additional users and attempt to log into client-1 with one of the users
—
Login to DC-1 as jane_admin
Open PowerShell_ise as an administrator
Create a new File and paste the contents of the script into it
Run the script and observe the accounts being created
When finished, open ADUC and observe the accounts in the appropriate OU　(_EMPLOYEES)
attempt to log into Client-1 with one of the accounts (take note of the password in the script)

