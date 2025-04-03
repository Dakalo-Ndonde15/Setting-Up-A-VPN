# Setting Up and Managing Office 365 for Small Business Operations

Objective: The goal of this homelab project is to simulate the deployment and management of Office 365 (now Microsoft 365) within a small business environment. This project will help you gain hands-on experience in setting up and configuring Office 365 services, managing users, securing data, and troubleshooting issues in a cloud-based environment.

Lessons Learned:

Cloud Admin Skills: Gained experience with Microsoft 365 Admin Center for user management and service configuration.
Security Best Practices: Implemented security measures such as MFA, conditional access, and data loss prevention.
Collaboration Tools Mastery: Set up Teams and OneDrive to improve team collaboration and file sharing.

Tools
Office 365 Admin (30 Day free trial)

https://www.microsoft.com/en-us/microsoft-365/business/microsoft-365-business-standard-one-month-trial 

## Task I. Office 365 Tenant Setup

### Step 1: Sign up for a Microsoft 365 Business trial

Sign up for a Microsoft 365 Business or Education trial. Set up the tenant with your domain name (if you have one) or use the default domain. Configure the basic tenant settings (language, region, etc.).

![image](https://github.com/user-attachments/assets/c7ec4ac2-6d22-455e-89ce-b96cb19c9871)

![image](https://github.com/user-attachments/assets/e0eae49d-2d67-403f-a680-43f2f913e07b)

## Task II. User Management

### Step 1: Create user accounts

Created a sample of 10 users for the practical lab. Using Ava Johnson as an example. Got a brief overview of her account and noticed that some fields are not filled in yet but they will be later on in the exercise. 

![image](https://github.com/user-attachments/assets/90074413-224f-4657-aaa3-7cb361f855bf)

![image](https://github.com/user-attachments/assets/3a06cdd8-a725-410b-b4b5-a2ec5ca9f94c)

![image](https://github.com/user-attachments/assets/5bff372b-0970-4e6d-85b6-c3cd8ec4ef0b)

### Step 2: Assign apprropriate licenses

I've assigned her the default Microsoft 365 Business Standard licenses, 14 of 25. Scrolled through the licenses to makes sure that she is only assigned the licenses that she'll need for her role. In our case she'll be given Help Desk, Teams, and User Admin roles and permissions. There is an option too fine tune her roles but in this practice we're only gonna go w/ what is available under Admin center access and not "show all by category".

![image](https://github.com/user-attachments/assets/0c82b42d-1727-4bfc-9645-f24de63c388d)

### Step 3: Setting up Security groups for organizing users

To set up security groups we first go to "Active teams and groups" on the left hand of the page under "Teams & groups" section. From there we go to the security groups tap and click "add a security group" to make a new one. Name the security group "Help Desk" and click next then create group.

![image](https://github.com/user-attachments/assets/250f39ab-6666-4748-90f7-de2cca27dfe6)

![image](https://github.com/user-attachments/assets/e96576dd-4b2e-40df-a9ce-b012e6f120aa)

![image](https://github.com/user-attachments/assets/c755e724-3c77-4040-a17e-f88141c46418)

![image](https://github.com/user-attachments/assets/dd2f1eee-addc-4fdb-8c5e-99611ec1b6f9)

## Task III. Email Setup (Exchange Online)

### Step 1: Configure mailboxes for the created users

To configure mailboxes for created users, we first go to the users section in the left-hand pane, select Users and then choose Active users. Select the user you want to configure the mailbox for, in our case it would be Ava Johnson. In the User details page, under Licenses and Apps, click apps on the bottom drop down section. Double check that the user is assigned the appropriate license that includes Exchange Online, which should be part of the Microsoft 365 Business Basic plan. After assigning the license, click Save to apply changes. The mailbox will be created automatically when the license is assigned. 

![image](https://github.com/user-attachments/assets/70da2423-a73d-411f-b73e-9975551629cc)

![image](https://github.com/user-attachments/assets/10c44270-2b27-4926-92f1-7e64a3e4923b)

### Step 2: Set up custom email domains

To set up a custom email domain we need to go to Setup in the admin center. Under Domains, select Add domain to add your domain to Microsoft 365. For example, I'm using veridiontech.com as a domain name. Once the domain is verified, go back to Active users, select the user, and update their User name to use the new domain (i.e. veridiontech.com)

![image](https://github.com/user-attachments/assets/304596da-19f0-48f2-83de-1618723a4373)

![image](https://github.com/user-attachments/assets/4366acd1-3167-4bc7-91ad-55c5ed9e8b85)

![image](https://github.com/user-attachments/assets/82940a0d-1b69-4f54-9763-f97643ada643)

### Step 3: Configure mail flow rules

To configure mail flow rules (to filter emails, redirect them, or set up security protocols), go to Exchange Admin Center which is towards the bottom of the page on the left-hand pane. In the Exchange Admin Center, select Mail flow and then choose Rules. From here, you create new rules for email routing and other configurations like blocking externl mail.

![image](https://github.com/user-attachments/assets/e7b49e13-029d-4cdd-b1c6-9e86e743262e)
![image](https://github.com/user-attachments/assets/a5445678-0fe3-455c-8f70-86dd11f86fd5)

![image](https://github.com/user-attachments/assets/684b3b59-1ee0-46c1-aa4b-61faf19bf3bc)

![image](https://github.com/user-attachments/assets/55fbfd91-0074-45fb-a7e7-714668baf167)

### Step 4: Implement DLP policies

To configure Data Loss Prevention (DLP) Policies we first go to the Microsoft Purview Compliance Portal. To get there we click on Compliance under Admin centers which will redirect us to Microsoft Purview. From there we look at the left-hand pane and find Data lifecycle management then we click on Policies > Retention Policies. Create a new retention policy by clicking on "+ New retention policy" > name it "1-Year-Email-Retention" (as an example). Keep hitting next till you get to Retention settings, or if you want to be more specific you can choose where to apply the policy. Under retention settings choose Retain items for a specific period, i.e. 365 days or 1 year. You can choose what happens after retention, either delete items automatically after the retention periood or retain items but do not delete them (for legal hold scenarios). Review the policy and click create to finalize. The policy will automatically apply to all mailboxes in Exchange Online based on the chosen settings, it'll take up to 24 hoours for the policies too take effect.

![image](https://github.com/user-attachments/assets/364c09c5-11b7-4029-a5d8-6dfb03028249)
![image](https://github.com/user-attachments/assets/627acd17-adc6-44e1-90f1-c3800054ea7c)

![image](https://github.com/user-attachments/assets/d43c8276-ae4f-4ae8-bed7-dfac36023260)

![image](https://github.com/user-attachments/assets/c60373de-b2a9-41dd-8df4-e19e46e617b6)

![image](https://github.com/user-attachments/assets/1093f111-aea5-4215-a080-dac0d4977f60)

## Task IV. Collaboration Setup (Teams & OneDrive)

Set up OneDrive for Business for file storage and sharing, and implement access controls.

### Step 1: Enable Microsoft Teams for Your Organization

To set up Microsoft Teams for internal communication we need to go to the left pane of Microsoft 365 Admin Center and find Teams. Under Org-wide settings, ensure that Microsoft Teams is turned ON.

![image](https://github.com/user-attachments/assets/11886caa-a65c-4732-b847-74b5510f0d88)

![image](https://github.com/user-attachments/assets/8885baff-7aab-4101-b700-3a24800f3095)

### Step 2: Create Teams and Channels for Departments/Projects

Open the Teams Admin center and navigate to Teams > Manage Teams > + Add Team. Choose Build a team from scratch or Create from an existing Microsoft 365 group. Set the Team Name, Description, and Privacy settings: private (only invited users can join), public (anyone in the organization can join), or org-wide (automatically adds all employees). Click create, then Add members (you can also assign owners). Once a team is created, set up channels for better organization. Open the newly created Team and click More options > Add channel. Name the channel (i.e. Project Alpha) then choose privacy settings: standard (visible too all team members), private (only specific members can access) or shared (external users can collaborate). 

![image](https://github.com/user-attachments/assets/f383dfe4-5f1c-47d6-a852-cf1c8ebed2e5)

![image](https://github.com/user-attachments/assets/7ca3335f-044e-4706-bbe4-44da8c40a10d)

![image](https://github.com/user-attachments/assets/2c1f0d7c-af57-4ee7-8e01-10808ba80423)

![image](https://github.com/user-attachments/assets/57029a9c-f192-47e1-a112-034c0a88b2f0)

### Step 3: Configure Messaging and File Sharing in Teams

In the Teams Admin Center, go to Messaging Policies then click on the group you want and customize settings like deleting messages, Giphy use, or read receipts. 

![image](https://github.com/user-attachments/assets/78d31423-8bed-4504-b4f0-d08e1fb629e2)

![image](https://github.com/user-attachments/assets/764745e8-933d-4760-8103-4944f29b0eb9)

Under Files in Teams, ensure file storages are integrated. Users can upload files, co-edit documents, and manage sharing permissions.

![image](https://github.com/user-attachments/assets/2029a0fa-a80b-4b3b-ab61-29deed615ee6)

### Step 4: Set up OneDrive for Business for file storage and sharing, and implement access controls

Open OneDrive Admin Center and under Storage, set the default quota per user. In OneDrive Admin Center > Sharing, choose: anyone (files can be shared externally with a link), new and existing guests (only specific external users can access) or only people in your organizaton (prevents external sharing). Users can sync their OneDrive files to their local drives via the OneDrive app,.

![image](https://github.com/user-attachments/assets/220ce923-99f1-4fc3-a1be-a5514ce87b57)

## Task V. Security & Compliance

### Step 1: Enable Multi-Factor Authentication (MFA) for users to secure accounts.

Go to Microsoft 365 Admin Center, navigate to users then active users and select a user (or multiple users). Click "MFA" (under more actions). In the Microsoft Entra admin center page, find the user(s) and click Enable. Confirm and notify the user, the user(s) will be prompted to set up MFA the next time they log in. 

![image](https://github.com/user-attachments/assets/c4bd229a-0247-418c-a39e-c6d06f2e5186)

![image](https://github.com/user-attachments/assets/b55749e9-48d5-42fa-ab53-38b142793e6f)

![image](https://github.com/user-attachments/assets/46c8376e-db69-44ac-b7c2-f7408a70eb6e)

![image](https://github.com/user-attachments/assets/2e2a4486-f5e4-4fad-9706-6bdba53eda55)

### Step 2 : Set up Microsoft Defender for Office 365 to protect against threats like phishing.

Go to Microsoft 365 defender, navigate to Email & Collaboration > Policies & Rules. Click on Threat Policies > Anti-Phishing. Click Create or Modify Default Policy. Configure the following: users & domains to protect (add your company domain and key users), impersonation protection (enable for CEO/CFO/HR to prevent spoofing), and actions (quarantine phishing emails instead of delivering them and notify users when an email is blocked). Save the policy.

![image](https://github.com/user-attachments/assets/57ee33f2-e89d-4852-8ea3-a84a6df6d590)

![image](https://github.com/user-attachments/assets/a03bf955-07b7-4b58-8855-fba1b309d8ae)

![image](https://github.com/user-attachments/assets/cdcb88b6-ca22-4c63-83a0-74ad14281d8e)

### Bonus Step 3: Enable Anti-Spam Policies

From Microsoft Defender go to Threat Policies > Anti-Spam. Enable External Email warning to alert users of outside emails. Increase spam filtering senstivity too block suspicious messages then save changes.

![image](https://github.com/user-attachments/assets/b1c2e60d-0871-4138-a44e-6dcd288d726c)

