# Active Directory Lab: Part 3  
## Setting Up Remote Desktop and Bulk User Creation  

### Overview  
In this part of the lab, I configured **Remote Desktop** access for non-administrative users and created multiple user accounts in bulk using PowerShell. These steps introduced efficient management of user accounts and enabled secure remote access for standard users.

---

### Steps Performed  

#### 1. Configuring Remote Desktop for Non-Administrative Users  
- Turned on **DC-1** and **Client-1** VMs in the Azure Portal.  
- Logged into **Client-1** as `mydomain.com\jane_admin`.  
- Opened **System Properties** and navigated to the **Remote Desktop** settings.  
- Enabled access for **Domain Users** to use Remote Desktop.  
- Verified that standard users could now log into **Client-1** via Remote Desktop.  

**Screenshot Placeholder: Remote Desktop Settings Screen**

#### 2. Bulk User Creation and Verification  
- Logged into **DC-1** as `mydomain.com\jane_admin`.  
- Opened **PowerShell ISE** as an administrator.  
- Created a new script file and pasted the provided bulk user creation script.  
- Executed the script and observed the automatic creation of user accounts.  

**Screenshot Placeholder: PowerShell Script and Execution**

- Verified the accounts in the `_EMPLOYEES` Organizational Unit (OU) within **Active Directory Users and Computers (ADUC)**.  

**Screenshot Placeholder: ADUC Showing Bulk-Added Accounts**

- Selected one of the new user accounts and logged into **Client-1** successfully.  

**Screenshot Placeholder: Login Confirmation on Client-1**

---

### What's Next  
In the next part of the lab, I will explore:  
- Simulating account lockouts and configuring account lockout thresholds via Group Policy.  
- Observing the effects of account lockouts in **Active Directory** and resolving them by unlocking and resetting accounts.  
- Enabling and disabling user accounts, and testing login functionality under each state.  
- Examining system logs on both the Domain Controller and Client Machine to better understand security operations and account activity.  
