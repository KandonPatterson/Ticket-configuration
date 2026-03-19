<img width="700" height="200" alt="image" src="https://github.com/user-attachments/assets/f25c540e-e85a-427a-ad3c-d121d5e29902" />

osTicket - Post-Installation Setup
----------------------------------
This guide walks through the post-install setup and configuration of osTicket, an open-source support ticketing platform.
----------------------------------

Operating Systems Used
* Windows 10 (21H2)

Objectives
---------------------
* Configure Roles & Permissions
* Configure Departments
* Configure Teams
* Configure settings (to allow anyone to create tickets)
* Configure Agents
* Configure SLA and Help Topics

Steps
--------------------------
1. Configure Roles and Permissions through the Admin tab.
2. If it says Agent at the top right of your screen, you will know you are on the Admin tab. ~ * <img width="198" height="34" alt="image" src="https://github.com/user-attachments/assets/32338f39-8712-4042-97a1-61d90887c7bd" />

<img width="883" height="585" alt="image" src="https://github.com/user-attachments/assets/e4d5df20-edc2-43ce-aed0-5e375d76b8c2" />

To control what agents can see or access in osTicket:
* Navigate to the Admin Panel.
* Click on Agents.
* Go to Roles.
* Open the Permissions tab.
* Adjust as needed to manage agent access.

💡 Use Roles and Permissions carefully to maintain security and appropriate access levels within your support system.

3. Teams are used to group agents for collaboration and ticket assignment across departments. To set up or manage Teams:

<img width="880" height="130" alt="image" src="https://github.com/user-attachments/assets/c141ec8e-c953-4c1a-9a77-aee152ef3717" />

* Navigate to the Admin Panel.
* Click on Teams in the navigation menu.
* Select an existing team to edit, or click Add New Team.
* Fill in the team details:
  - Name – e.g., "Level 2 Support", "Escalations Team"
  - Team Lead – the agent responsible for overseeing the team
  - Members – select agents to include in the team
* Define the team's access level and assign them to specific departments if needed.
* Click Save Changes to apply the configuration.

💡 Teams are useful for organizing agents by expertise or responsibility, especially when tickets span multiple departments or require escalation.

4. Unrestrict ticket creation so anyone can submit tickets

<img width="879" height="562" alt="image" src="https://github.com/user-attachments/assets/6b356769-d942-426a-8578-d20b72994498" />

By default, osTicket may restrict ticket creation to registered users or authenticated agents. To allow anyone to create tickets (e.g., via the web form or email):

* Go to the Admin Panel.
* Under the Registration or User Authentication section:
  - Ensure that "Require registration/login to open tickets" is unchecked.
* Click Save Changes to apply the new settings.

Optional:
To accept tickets via email from unregistered users:
  * Go to Emails > Email Settings.
  * Make sure you have at least one email address configured and enabled for ticket creation.
  * Ensure your mail fetching (POP/IMAP) is working so incoming emails generate tickets.

⚠️ Allowing unrestricted ticket creation may increase the risk of spam. Consider enabling CAPTCHA or using a spam filter.

5. Configure Agents
<img width="880" height="793" alt="image" src="https://github.com/user-attachments/assets/43b41cf3-881f-4abb-986e-1b39971aa64d" />

Steps to Configure Agents:
  * Navigate to the Admin Panel.
  * Click on Agents in the sidebar menu.
  * Choose an existing agent to edit, or click Add New Agent.
  * Enter the agent’s details:
    - Full Name
    - Email Address
    - Username and Password
    - Primary Department (determines initial ticket access)
  * Assign Roles:
     ~ Roles define what the agent can see and do in the system (e.g., Admin, Support Staff). ~
  * (Optional) Assign the agent to one or more Teams for collaborative ticket handling.
  * Click Save Changes to apply the configuration.
   💡 Use Roles and Departments strategically to control access and responsibilities across your support team.

 6. Configuring SLA Plans in osTicket

    ~ SLA (Service Level Agreement) Plans define the expected response and resolution times for tickets. They help prioritize support and measure performance. ~

    <img width="883" height="540" alt="image" src="https://github.com/user-attachments/assets/639569ec-94c3-4a14-ad6d-f2c49ff0739b" />

    Steps to Configure SLA Plans:
    * Go to the Admin Panel.
    * Click on Manage > SLA Plans.
    * Click Add New SLA Plan.
    * Fill in the following fields:
      - Name – e.g., "Standard", "Priority Support"
      - Grace Period – time allowed to respond or resolve (in hours)
      - Schedule – choose when the SLA applies (business hours, weekends, etc.)
    * Click Save Changes.
      💡 You can assign SLA Plans to Help Topics, Departments, or Tickets directly for automated prioritization.

      Help Topics allow you to categorize incoming tickets and automatically assign departments, priorities, or SLA plans based on the topic selected by the user.

      <img width="877" height="511" alt="image" src="https://github.com/user-attachments/assets/1a5e6421-f238-4093-800a-df46bee7c6ab" />

      Steps to Configure Help Topics:
        * Go to the Admin Panel.
        * Click on Manage > Help Topics.
        * Fill in the following:
           - Topic Name – e.g., "Technical Support", "Billing Inquiry"
           - (Optional) Parent Topic – for creating a hierarchy of topics
           - Department – auto-assigns tickets to the selected department
           - Priority – set default urgency
           - SLA Plan – apply an SLA automatically
           - Auto-assign – select an agent or team
        *  Click Save Changes
        💡 Help Topics streamline ticket routing and ensure tickets go to the right team with the appropriate urgency.

      Your osTicket help system should now be functional, organized, and ready to tackle incoming requests.





















































