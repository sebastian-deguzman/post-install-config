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

Awesome now that osTicket is installed successfully on our virtual machine we will now set system administrative tasks within our osTicket. Once were logged in as an admin, to configure the roles within the site well go to "admin panel" > agents > roles

![Screenshot 2025-04-25 042746](https://github.com/user-attachments/assets/ce12bdab-bdb1-4ad4-861b-d1827b645818)

From the role page we will add a new role and name it Supreme Admin

![Screenshot 2025-04-25 043003](https://github.com/user-attachments/assets/f4fc8e04-6026-4571-9663-0da31c033ad3)

Then in the same page click permissions and check all boxes granting full access to everything grantinng full administrative access.

![Screenshot 2025-04-25 043205](https://github.com/user-attachments/assets/682da582-74fb-4659-ac71-5c9b3e5bafc9)

Back to the agents tab we will now click Departments. From Deparments we will name it "Support/SysAdmins"

![Screenshot 2025-04-25 045838](https://github.com/user-attachments/assets/c8a9721e-3afb-4e6d-8da8-451578b6b46d)

Great now that we've created that were goign to create "teams". On the teams tab click "add new team" and we will name it online banking

![Screenshot 2025-04-25 050639](https://github.com/user-attachments/assets/60358255-0403-43a6-ba7b-8e476455ce9e)

We will now continue to create agents (workers). so to do this on the admin panel > agents > add new agent
for the credentials well use Andrew Smith with username: andrewsmith / password: Password1

![Screenshot 2025-04-25 050935](https://github.com/user-attachments/assets/47aa6245-7676-4ded-82ef-2efb508ad5be)

Now under access we will put Andrew Smith in the SysAdmins dept and give him Supreme Admin. On the same page click teams and add him to Online Banking.

![Screenshot 2025-04-25 051230](https://github.com/user-attachments/assets/33fddb40-aa49-4c69-92c2-2ec289117c55)

Now we are going to create another worker in annother department. Under agents > add new well do the same thing but with Tullio Parry and we will add him in the Support department also under onlinebanking. Once done, we should have 2 workers in 2 different departments.

![Screenshot 2025-04-25 051642](https://github.com/user-attachments/assets/65531de6-ae16-4c94-9f43-8a365b988881)

Fantastic! now that we have our agents we can configure our SLA protocol, this helps us distinguish the urgency of each ticket. to do this, under manage > SLA > add new SLA plan
we will now add our first SLA plan named: Sev-A (grace period: 1 hour, scheduled 24/7)

![Screenshot 2025-04-25 052054](https://github.com/user-attachments/assets/4c352a0d-32f2-46a4-80a7-7bc7b1a657d1)


we will continue to repeat the same steps to add 2 more SLA plans. Sev-B (4 hour, 24/7), Sev-C (8 hour, business hours mon-fr 9-5)

![Screenshot 2025-04-25 052259](https://github.com/user-attachments/assets/2651ee5f-ed93-41e3-b73f-c51226c9fd3f)

Once completed well configure Help topics. This allows users to create a ticket. Under Manage > help topics > add new (we will add the following): business critical outage, Personal computer issues, equpiment request, password reset, other

![Screenshot 2025-04-25 054145](https://github.com/user-attachments/assets/f893a1ad-84e4-4436-a518-e955c6b8a9ab)

And there you have it! our osTicket help desk system now has departments and agents working in our system!

![Screenshot 2025-04-25 054201](https://github.com/user-attachments/assets/8e6b5ae0-130f-40ff-b4f9-29f26975d976)

