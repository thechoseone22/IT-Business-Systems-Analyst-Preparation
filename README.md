# IT-Business-Systems-Analyst-Preparation
## 🚀 Summary: Steps I Can Take Right Now

1. **Tonight or Tomorrow**: Set up a virtual machine and start a home lab.
2. **Within 2-3 Days**: Explore Odoo or Floreant POS for hands-on ERP/POS practice.
3. **This Week**: Watch intro videos on PMS and ERP systems in hospitality.
4. **Track It All**: Use Trello or Notion to organize your progress
- [x]  Setup project manager to track progress

### 1. **Home Lab Setup** (Start Tonight or Tomorrow)

Setting up a basic IT systems lab on your own computer

---

**Goal:** Simulate enterprise user access management and security implementation

**What I Did:**

- Installed Windows Server 2025 and configured it as a Domain Controller (`derek.lab`)
- Created organizational users and security groups in Active Directory
- Enforced password policies and disabled system access through Group Policy
- Tested user authentication, folder access, and policy enforcement
    
    **Result:** Hands-on experience with enterprise-grade identity management and application security relevant to IT analyst roles
    

---

- **Download VirtualBox or VMware Workstation Player** (Free)
- [x]  Set up a few virtual machines (e.g., Windows 11, Windows Server, Linux, Ubuntu)
- Downloaded and installed windows 11, as well as windows server 2025 using VirtualBox. I connected the w11 install to the windows server successfully.

![virtual box.png](attachment:f5f9be7f-017d-4287-9a25-741e0dae099a:virtual_box.png)

![user control panel access.png](attachment:45e3a096-a791-433a-839b-bea4f018f1bf:user_control_panel_access.png)

- Learn:
    - [x]  How to create user roles
        - I created individual/organizational users like John Smith, Anthony Davis and added them to security groups  like HR as shown below
        - This simulates users roles just like in a real company (role-based access control)
        
        ![user roles.png](attachment:d0bc1772-e8c0-4089-8fbe-12ab0f37b6b4:user_roles.png)
        
    
    - [x]  How to restrict access to files or folders (simulate access control)
        - Tested real-world access control as seen below
    
    ![NTFS permissions.png](attachment:93d071bd-6a52-4340-ab5b-7808668d9b13:NTFS_permissions.png)
    
    - [x]  Basic server/network configuration
        - I’ve configured the server as shown above/earlier and installed the OS, given it a static IP. When promoting to Domain Controller, the system sets up the DNS, networking etc.
        - I configured core services on a virtual enterprise-grade server. This is the same as the real world stuff but safer to use as it is virtually on my pc.
            
            ![server setup.png](attachment:12674255-e633-4b2a-ba5e-fbbba5f94903:server_setup.png)
            

---

Here is other numerous tests/learning I’ve done:

- Server/Client IPs and ping test
    
    ![ping test.png](attachment:deb5e294-a013-49cb-8459-7ca4c5d1d0a9:ping_test.png)
    
- Shared folder permissions
    
    ![NTFS permissions.png](attachment:decbf3ad-45b2-494b-8acc-45dff66c1586:NTFS_permissions.png)
    
- Group Policy settings
    
    ![group policy settings.png](attachment:a0308843-3d6a-48c8-b235-e4b8bee26a57:group_policy_settings.png)
    
    ![usb access.png](attachment:4c33dccd-8892-4a57-aa69-790d3a2bbb55:usb_access.png)
    
    ![logonhours.png](attachment:fc2cbc47-6b39-412d-9b6d-45b8f41d6d8d:logonhours.png)
    
- Domain-joined system info: this is visible in multiple screenshots
- User login tests

![user control panel access.png](attachment:63af8380-f612-4fd1-88e5-d729f00977c2:user_control_panel_access.png)

- Reflection
    - What I’ve learned the most from this was understanding how crucial troubleshooting and getting hands-on experience is to understanding new skills. There was so many times where I was stuck and I had to look up what the issue was. Going through the troubleshooting steps helped me learn so much and was very satisfying in the end finally solving it! Learning why the ping test isn’t working, how user and group policies impact system security across different departments; this made me realize how important testing and configuration is in real-world IT environments.

## **Next Steps:**

- Set up **Windows Admin Center** to manage your server through a browser
- Try simulating a **remote access VPN**
- Add a **Linux VM** to your internal network and manage cross-platform access
- Or simulate a **ticket-based helpdesk issue** and document how you resolved it

# 2. **Free ERP/POS Simulations**

Demo real ERP systems online:

- [ ]  [**Odoo.com**](https://www.odoo.com/) – Free ERP sandbox (inventory, accounting, sales, etc.)
- [x]  [**Floreant POS**](http://floreant.org/) – Open-source POS software you can install and explore locally
    - Installed MySQL software and needed plugins(MySQL Server, Workbench, Shell, and other helpful tools)
    - Created database using command line interface as it uses SQL as its language mode by default and automatically connects to your database server, I also tried connecting to the database server manually in MySQL Shell to gain experience as seen below.
        
        ![By contrast MySQL shell does not auto connect to the database server and opens in JavaScript mode, not SQL. You have to connect manually using the command:”\connect [root@localhost](mailto:root@localhost)” and then switch to SQL mode using:”\sql”](attachment:d0f6e975-7041-4dcb-92eb-694ab2fbb243:CLI_AND_SHELL.png)
        
        By contrast MySQL shell does not auto connect to the database server and opens in JavaScript mode, not SQL. You have to connect manually using the command:”\connect [root@localhost](mailto:root@localhost)” and then switch to SQL mode using:”\sql”
        

## Summary

| Tool | Behavior |
| --- | --- |
| **MySQL Command Line Client (classic/legacy client aka mysql.exe)** | Connects automatically to SQL and runs commands right away as it asks your root password aka server password immediately |
| **MySQL Shell** | Defaults to JS, needs manual connection and mode switch |
- Menu Management, Modifier groups, sales receipt, database confirmation

- Pivoted to Floreant POS as chasing one error was too time consuming

- Connected ORO POS to MySQL database
    
    ![database connection.png](attachment:1ff1787b-621b-49e1-986e-98277010fbea:database_connection.png)
    
- Reflection: what suprised me the most about setting up the database was how many technical knowledge is needed when something goes wrong. Research is definitely needed, as I had a lot of trouble with missing drivers in the ORO POS batch file.
- I independently installed and configured a full POS system (ORO POS 1.6.4) integrated with MySQL 8.0.41, resolving driver compatibility issues, editing batch launch scripts, and managing secure user/database interaction through SQL. This helped me better understand real-world enterprise system deployment and sharpened my debugging workflow. Here are some technical skills I gained below:
    - Installed and configured MySQL 8.0.41
    - Created a custom user with privilege management
    - Integrated a Java-based POS system (ORO POS) with a database backend
    - Manually configured JDBC connector (troubleshooting versioning & classpath issues)
    - Used the command line for user creation, shell access, and permissions
    - Edited and tested Windows batch scripts (`.bat`)
    - Verified Java classpath resolution using `dir` and `echo` debugging
    
    Here is further documentation of my learning experience connecting ORO POS to MySQL database:
    
    ![batch script, echo, and driver issues.png](attachment:31c3c16b-c5a0-4392-8f0e-00e7694745c3:batch_script_echo_and_driver_issues.png)
    
    ### **System Troubleshooting & Problem Solving**
    
    - Resolved a `Connection failed` to the ORO POS database error by:
        - Diagnosing driver load issues
        - Testing user-level access from CLI
        - Debugging ORO POS environment with custom script changes
    - Identified and fixed mismatches in connector versions (`mysql-connector-j vs java`)
    - Navigated JDBC/MySQL compatibility issues manually
    
    ---
    
    ### **Security Awareness**
    
    - Learned about **database users**, host restrictions, and access scopes
    - Understood how **ORO POS uses a “secret key”** for secure login/config
    - Practiced basic **least-privilege principle** by avoiding `root` for POS login
    
    ---
    
    ### **Enterprise Application Deployment Experience**
    
    effectively built a **local production-ready POS system**
    
    - Effectively built a **local production-ready POS system**
    - Understood how enterprise software separates:
        - Frontend UI
        - Backend DB
        - Middleware/driver communication
    
    ---
    
    ### **Soft Skills Practiced**
    
    - Persistence through trial and error
    - Problem decomposition
    - Reading documentation and interpreting ambiguous instructions
    - Documenting a repeatable process for future users
    
    # New software: Floreant POS instead of ORO POS (fork of Floreant)
    
- Could not get adding new menu items to work so I moved to this software
- Ran into the same error as above but was resolved easily
- Practiced Menu Management, Modifier Groups, Created Users,  Receipts, and database confirmation(bonus)
    - POS System is fully functional for test sales with MySQL backend

![Menu Management flor.png](attachment:c0396a3a-a18e-4761-98c9-f97ff017c0ff:Menu_Management_flor.png)

![Modifier group flor.png](attachment:26414438-6daf-48b8-87e2-bf7f7a246662:Modifier_group_flor.png)

![RECEIPT.png](attachment:7e741b8e-d5c7-424f-850c-03611cbb8d74:RECEIPT.png)

![DATABASE CONF FLOR.png](attachment:3b6b496c-72b6-49af-9f77-4f9d571a55fe:DATABASE_CONF_FLOR.png)

![DATABASE CONF FLOR 2.png](attachment:d570b818-87a7-4c57-a548-baca29bf39b6:DATABASE_CONF_FLOR_2.png)

# **3. This Week**: Watch intro videos on PMS and ERP systems in hospitality.
