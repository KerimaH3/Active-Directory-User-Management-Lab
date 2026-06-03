# Active-Directory-User-Management-Lab
# Overview
Built a windows Server 2022 Active Directory home lab using VirtualBox to simulate a corporate IT environment. Configured Active Directory Domain Services (AD DS), DNS, Organizational Units (OUs), users, security groups, shared folders, and access permissions. Joined a windows workstation to the domain and verified user access to network resources. 

# Lab Environment
# Domain Controller

# Item            Value
  Hostname        DC01
  OS	            Windows Server 2022
  Domain	        corp.local
  IP Address	    192.168.56.10

# Client Workstation

# Item            Value
  Hostname        LAB-WIN11
  OS              Windows 11
  Domain          corp.local
  IP Address      192.168.56.20

# Virtualization Platform

- Oracle VirtualBox
- Internal Network Adapter

# Objectives

- Build a Windows Server Active Directory environment
- Configure DNS services
- Create and manage users
- Create and manage security groups
- Organize users with OUs
- Join client computers to the domain
- Configure shared folders
- Apply NTFS permissions
- Verify user access through group membership

# Technologies Used

- Windows Server 2022
- Windows 11
- Active Directory Domain Services (AD DS)
- DNS
- Active Directory Users and Computers (ADUC)
- NTFS Permissions
- Shared Folders
- Oracle VirtualBox
- Command Prompt
- PowerShell

# Tasks Completed

# 1. Installed and Configured Active Directory
- Installed AD DS role
- Promoted server to Domain Controller
- Created domain: corp.local
  
 <img src="screenshots/domain-controller-setup.png" width="600"> 

# 2. Configured DNS
Configured DNS services automatically during AD DS installation.

Verified DNS resolution using: nslookup corp.local

 <img src="screenshots/dns.png" width="600"> 

# 3. Created Organizational Units (OUs)
Created department-based OUs:

- HR
- IT
- Sales
  
 <img src="screenshots/organizational-units.png" width="600"> 

# 4. Created Users
Created test users including:

- Amelia Oliver
- Jarod Lee
- Sophia Lucas
- Olivia Noah


 <img src="screenshots/users.png" width="600"> 

# 5. Created Security Groups
Created:

IT_Admins
Assigned IT Admins to the group.

 <img src="screenshots//security-groups.png" width="600"> 

# 6. Moved Users into OUs
Organized users into departmental OUs.

 <img src="screenshots//user-management.png" width="600"> 


# 7. Joined Windows 11 Workstation to Domain
Joined LAB-WIN11 to:

corp.local
Verified successful authentication.

 <img src="screenshots//network-testing.png" width="600"> 

# 8. Verified Network Connectivity
Verified communication between LAB-WIN11 and DC01.

Commands used:

- ipconfig /all
- ping 192.168.56.10
- nslookup corp.local
  
 <img src="screenshots//domain-join.png" width="600"> 

# 9. Created Shared Folder
Created:

C:\Shares\HR
Shared as:

HR-Share

 <img src="screenshots//shared-folder.png" width="600"> 

# 10. Configured Share Permissions
Granted access to:

HR_Users
Permissions:

- Read
- Change
 <img src="screenshots//share-permission.png" width="600"> 

# 11. Configured NTFS Permissions
Granted HR_Users:

- Modify
- Read
- Write
- Read & Execute
- 
<img src="screenshots//ntfs-permissions.png" width="600"> 

# 12. Verified Access from Client Workstation
Logged into LAB-WIN11 as:

corp\olivia.noah
Accessed:

\\DC01\HR-Share
Created:

TestFile.txt
Successfully verified:

- Authentication
- Group Membership
- Share Permissions
- NTFS Permissions

<img src="screenshots///access-verification.png" width="600"> 

# Skills Demonstrated
- ctive Directory Administration
- Windows Server Administration
- User and Group Management
- DNS Configuration
- Domain Management
- Organizational Unit Management
- Shared Folder Management
- NTFS Permissions
- Access Control
- Troubleshooting
- Help Desk Fundamentals
- Windows Networking

# Project Outcome
Successfully built and managed a Windows Active Directory environment, joined a workstation to the domain, configured access controls, and verified secure access to shared resources using Active Directory security groups and NTFS permissions.
