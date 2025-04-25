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

- Windows 10</b> (22H2)

<h2>Post-Install Configuration Objectives</h2>

- Roles
- Departments
- Teams
- Agents (workers)
- Users (customers)
- Help Topics
- Service Level Agreements (SLAs)

<h2>Configuration Steps</h2>

Awesome now that osTicket is installed successfully on our virtual machine we will nonw set system administrative tasks within our osTicket. Once were logged in as an admin, to configure the roles within the site well go to "admin panel" > agents > roles


From the role page we will add a new role and name it Supreme Admin


Then in the same page click permissions and check all boxes granting full access to everything grantinng full administrative access.


Back to the agents tab we will now click Departments. From Deparments we will name it "Support/SysAdmins"


Great now that we've created that were goign to create "teams". On the teams tab click "add new team" and we will name it online banking

We will now continue to create agents (workers). so to do this on the admin panel > agents > add new agent
for the credentials well use Andrew Smith with username: andrewsmith / password: Password1


Now under access we will put Andrew Smith in the SysAdmins dept and give him Supreme Admin. On the same page click teams and add him to Online Banking.


Now we are going to create another worker in annother department. Under agents > add new well do the same thing but with Tullio Parry and we will add him in the Support department also under onlinebanking. Once done, we should have 2 workers in 2 different departments.

Fantastic! now that we have our agents we can configure our SLA protocol, this helps us distinguish the urgency of each ticket. to do this, under manage > SLA > add new SLA plan
we will now add our first SLA plan named: Sev-A (grace period: 1 hour, scheduled 24/7)


we will continue to repeat the same steps to add 2 more SLA plans. Sev-B (4 hour, 24/7), Sev-C (8 hour, business hours mon-fr 9-5)


Once completed well configure Help topics. This allows users to create a ticket. Under Manage > help topics > add new (we will add the following): business critical outage, Personal computer issues, equpiment request, password reset, other

