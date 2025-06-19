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

![step11](https://github.com/user-attachments/assets/93594da9-1f71-407f-9952-61e8457129ee)


### Restart and then log back into DC-1 as user: mydomain.com\labuser


### Create a Domain Admin user within the domain
![step12](https://github.com/user-attachments/assets/29691f8c-840c-491c-bd55-10dc21b4fc32)

![step13](https://github.com/user-attachments/assets/34d44ec3-43bb-4b5f-8180-a07557534be6)

![step14](https://github.com/user-attachments/assets/974db0fa-a10c-42ed-88c9-8ff0af287b28)

![step15](https://github.com/user-attachments/assets/53f269d0-7d7e-4107-abaf-59c11f3080fc)

![step16](https://github.com/user-attachments/assets/6b1dbd16-4196-4b5c-b1f4-c4668035702a)

![step17](https://github.com/user-attachments/assets/21504901-8490-4ee3-a6a0-f7df6983eda3)

![step18](https://github.com/user-attachments/assets/47975957-29a0-4ebc-a174-97a5f4dea48b)

![step19](https://github.com/user-attachments/assets/4996326d-a737-4a1c-b74a-eb6f736885c6)

![step20](https://github.com/user-attachments/assets/c635565d-474f-48c3-aa55-b86aa0021555)

—
### In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called “_EMPLOYEES”

![step21](https://github.com/user-attachments/assets/46c9ef83-b71f-4ac8-853f-ed7e39218653)

![step22](https://github.com/user-attachments/assets/fa303e5b-259e-4a18-be13-ac0ba1fa57d7)



### Create a new OU named “_ADMINS”
### Repeat the same steps up above


### Create a new employee named “Jane Doe” (same password) with the username of “jane_admin” / Cyberlab123!

![step24](https://github.com/user-attachments/assets/f3dcb5db-eb83-4787-b0d3-cd0b78f764e0)

![step25](https://github.com/user-attachments/assets/9ad127e4-313f-4670-8099-0e3a9dbcc005)

![step26](https://github.com/user-attachments/assets/24a582c5-d387-4fcf-93e0-0c1349a0f5c6)

![step27](https://github.com/user-attachments/assets/5150454d-0f75-47c2-b210-984cdb36d86a)

#### Add jane_admin to the “Domain Admins” Security Group

![step28](https://github.com/user-attachments/assets/898f5439-3ef4-4d87-9671-3d87b5afcea5)

![step29](https://github.com/user-attachments/assets/dbaa9de7-1baf-43d0-8635-b8c6ca9aa06d)

### Log out / close the connection to DC-1 and log back in as “mydomain.com\jane_admin”

### User jane_admin as your admin account from now on


### Join Client-1 to your domain (mydomain.com)
—
### From the Azure Portal, set Client-1’s DNS settings to the DC’s Private IP address (Already done)
### From the Azure Portal, restart Client-1 (Already done)

### Login to Client-1 as the original local admin (labuser) and join it to the domain (computer will restart)

![step30](https://github.com/user-attachments/assets/127fa2d7-0235-4718-ab4d-471fe1a9dca5)

![step31](https://github.com/user-attachments/assets/24d75b80-a593-4d4d-9082-37217e058eb5)

![step32](https://github.com/user-attachments/assets/fd711204-8e62-43ad-af34-edfadebfdc9c)

![step33](https://github.com/user-attachments/assets/9e481c82-4173-4b34-bee3-90a99a0dc2e2)

### Login to the Domain Controller and verify Client-1 shows up in ADUC
### Create a new OU named “_CLIENTS” and drag Client-1 into there

![step35](https://github.com/user-attachments/assets/ca7178a6-c328-4a31-ba0e-85166fd29bb2)

![step36](https://github.com/user-attachments/assets/7fb047bb-7c9d-4c28-a952-e6d5336e20ee)

![step37](https://github.com/user-attachments/assets/417b4b9b-9957-44a1-899d-29f04d7b9f06)

![stpe34](https://github.com/user-attachments/assets/f9b3e30b-20bf-4a90-b7da-708bedb97474)

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

` # ----- Edit these Variables for your own Use Case ----- #
$PASSWORD_FOR_USERS   = "Password1"
$NUMBER_OF_ACCOUNTS_TO_CREATE = 10000
# ------------------------------------------------------ #

Function generate-random-name() {
    $consonants = @('b','c','d','f','g','h','j','k','l','m','n','p','q','r','s','t','v','w','x','z')
    $vowels = @('a','e','i','o','u','y')
    $nameLength = Get-Random -Minimum 3 -Maximum 7
    $count = 0
    $name = ""

    while ($count -lt $nameLength) {
        if ($($count % 2) -eq 0) {
            $name += $consonants[$(Get-Random -Minimum 0 -Maximum $($consonants.Count - 1))]
        }
        else {
            $name += $vowels[$(Get-Random -Minimum 0 -Maximum $($vowels.Count - 1))]
        }
        $count++
    }

    return $name

}

$count = 1
while ($count -lt $NUMBER_OF_ACCOUNTS_TO_CREATE) {
    $fisrtName = generate-random-name
    $lastName = generate-random-name
    $username = $fisrtName + '.' + $lastName
    $password = ConvertTo-SecureString $PASSWORD_FOR_USERS -AsPlainText -Force

    Write-Host "Creating user: $($username)" -BackgroundColor Black -ForegroundColor Cyan
    
    New-AdUser -AccountPassword $password `
               -GivenName $firstName `
               -Surname $lastName `
               -DisplayName $username `
               -Name $username `
               -EmployeeID $username `
               -PasswordNeverExpires $true `
               -Path "ou=_EMPLOYEES,$(([ADSI]`"").distinguishedName)" `
               -Enabled $true
    $count++
}
`
Run the script and observe the accounts being created
When finished, open ADUC and observe the accounts in the appropriate OU　(_EMPLOYEES)
attempt to log into Client-1 with one of the accounts (take note of the password in the script)

