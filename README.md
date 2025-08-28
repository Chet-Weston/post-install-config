<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>
 
- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles (for grouping permissions), Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking) & teams 
- Allow anyone to create/submit a ticket
- Configure Agents (workers) & Configure Users (customers)
- Configure SLA & Help Topics 

<h4>**Make note of the difference between Admin/Anylist Login Page vs the End Users osTicket page**</h4>

<h2>Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/fuXnzPD.png" height="80%" width="80%" alt="Configure Roles & Teams"/>
</p>
<p>
In osTicket, make sure you are in the Admin page. Start by navigating to (Agents --> Roles) and selecting "New Role." Here, you can name the Role whatever fits the role to be assigned. For this example, we will use "Supreme Admin". Once named, you will be able to select certain roles that they will be allowed to fulfill. Next, locate the Departments (Admin Panel --> Agents --> Departments). Create a new Department, For this example, we will be using the name "SysAdmins". And from the Access panel, you can add certain people to each department. Next navigate to Teams (Agents --> Teams) This allows you to pull agents from different departments into the same team. For this example, it's named "Online Banking" 
</p>
<br />

<p>
<img src="https://i.imgur.com/hlqmNDZ.png" height="80%" width="80%" alt="Create & submitting Tickets"/>
</p>
<p>
Navigate the following path (Admin panel --> Settings --> User) **UNCHECK unregistered users can create tickets**. Registration required: Requires registration and login to create tickets.  
</p>
<br />

<p>
<img src="https://i.imgur.com/CeTawdv.png" height="80%" width="80%" alt="Configure Agents & Users "/>
</p>
<p>
(Admin panel --> Agents --> Add New) Create 2 agents, Jane Doe (dept. SysAdmins) & John Doe (dept. Support). Once in the "Add New Agent Panel," Fill out the requested info for the Agents being added. For Jane, select in the "access" panel for their primary department "SysAdmins" and the Role of "Supreme Admin." Lastly, in the Teams panel, select "Online Banking" as their assigned team, and create this User. Once completed, create another Agent "John Doe"  with the following permissions and Departments. (Department: Support Role: View Only Team: N/A). Once both Agents have been created in their respective account settings, you can set their passwords. Unselect "Send the agent a password reset email" and type in the password you wish to use.
Once the Agents have been added, now we have to add "Users" start by going to the Agents window of osTicket. and finding the Users panel. From here, select "Add User" and create 2 new users (Karen & Ken) 
To create a new user, you will need to add an email address associated with the user.  
</p>
<br />

<p>
<img src="https://i.imgur.com/8yrsql5.png" height="80%" width="80%" alt="Configure SLA & Help Topics "/>
</p>
<p>
Next, we are going to create a Service Level Agreement (SLA). This is set and used by departments to ensure that tickets get prioritized and managed in a correct and timely manner. 
To do this, navigate to the "Admin panel" (Manage --> SLA --> Add new SLA). Add in 3 new SLAs.
<br /> Sev-A: Grace Period: 1 Hr, Schedule: 24/7 
<br /> Sev-B: Grace Period: 4 Hrs, Schedule: 24/7 
<br /> Sev-C: Grace Period: 8 Hrs, Schedule: Business Hours)
<br /> The last thing for this lab to be done is "Configuring Help Topics" (For when users create tickets), (Admin Panel --> Manage --> Help Topics --> Add New Help Topic). Create the following Help Topics 
<br /> Business Critical Outage, Personal Computer Issues, Equipment Request, Password Reset & Other.
<br /> With those steps being completed, now we have a baseline for our Helpdesk to operate. We have added Roles, Departments & Teams to handle any request that Users would have submitted tickets for, as well as having the SLA & Help Topics to make sure that the tickets that are submitted are done in an appropriate amount of time and prioritized correctly.
  
</p>
<br />
