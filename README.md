<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Installation & Configuration in Minutes!</h1>
This setup involves installing Active Directory Domain Services on DC-1, promoting it as a domain controller for the domain mydomain.com, creating organizational units for EMPLOYEES, ADMINS, and CLIENTS, adding a new employee to the Domain Admins group, joining Client-1 to the domain, organizing it within the CLIENTS OU, configuring access for non-administrative users, and using PowerShell to create additional users in the EMPLOYEES OU, followed by attempting to log into Client-1 with one of these new users.<br />


<h2>Video Demonstration</h2>

https://youtu.be/37QgVYfFlTg

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell ISE

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Installation and Configuration Steps</h2>

1. Install Active Directory Domain Services Inside DC-1 and Promote it as a domain controller (mydomain.com)

2. Create Organizational Units called EMPLOYEES, ADMINS and CLIENTS

3. Create a new employee named Jane Doe and add her to the Domain Admins Security Group

4. Login to Client-1 and join it to the domain (mydomain.com)

5. Login to DC-1, verify Client-1 is Joined, and copy it into the organizational Units called CLIENTS

6. Configure Client-1 so that non-administrative Users can access

7. Create additional users inside the organizational Units called EMPLOYEES with PowerShell script and attempt to log into client-1 with one of the users.
   

<h2>Deployment and Configuration Steps</h2>

<h2>Install Active Directory Domain Services Inside DC-1 and Promote it as a domain controller</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
This setup involves installing Active Directory Domain Services (AD DS) on the DC-1 virtual machine and promoting it to a domain controller for the domain mydomain.com. Once promoted, DC-1 takes on the role of managing and storing the directory information for the domain, handling user authentication, authorization, and other essential services like DNS for domain-joined computers. This process also configures the domain controller to support network management, security policies, and resource access for users and computers within the mydomain.com domain.
</p>
<br />

<h2>Create Organizational Units called EMPLOYEES, ADMINS and CLIENTS</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, Organizational Units (OUs) named EMPLOYEES, ADMINS, and CLIENTS are created within Active Directory to logically organize and manage different groups of users and resources based on their roles or functions within the domain. EMPLOYEES could include regular staff members, ADMINS would contain administrative accounts with higher privileges, and CLIENTS might include machines or users that require different access levels or management. Organizing resources into OUs helps simplify administration, apply specific group policies, and delegate management tasks based on the role of each group.
</p>
<br />

<h2>Create a new employee named Jane Doe and add her to the Domain Admins Security Group</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, a new user account for Jane Doe is created in Active Directory, and she is assigned to the Domain Admins Security Group. By adding her to this group, Jane Doe is granted full administrative privileges over the domain, allowing her to manage domain settings, users, and other resources across the network. This step ensures that she has the necessary permissions to perform high-level administrative tasks within the domain, such as managing user accounts, group policies, and server configurations.
</p>
<br />

<h2>Login to Client-1 and join it to the domain</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I logged into Client-1 and join it to the mydomain.com domain by configuring its system settings to communicate with the domain controller. This action allows Client-1 to become part of the domain, enabling it to use domain-based authentication, access network resources, and receive domain policies. By joining the domain, Client-1 can be centrally managed through Active Directory, allowing for easier administration and user access control within the network.
</p>
<br />

<h2>Login to DC-1, verify Client-1 is Joined, and copy it into the organizational Units called CLIENTS</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I logged into DC-1, the domain controller, and confirm that Client-1 has been successfully joined to the mydomain.com domain by checking its status in Active Directory. After verification, Client-1 is moved into the CLIENTS organizational unit (OU), which helps organize and manage the client machine within the domain. Placing Client-1 in the CLIENTS OU ensures that it can inherit specific group policies and permissions designed for client devices, making it easier to manage access and apply configurations for that particular group.
</p>
<br />

<h2>Configure Client-1 so that non-administrative Users can access</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, Client-1 is configured to allow access for non-administrative users by modifying the machine's permissions, group memberships, and local user settings. This typically involves ensuring that users who are not part of the Administrators group can still log in and access necessary resources while restricting access to sensitive administrative functions. By configuring these settings, Client-1 ensures that non-administrative users have the necessary rights to perform their tasks, such as running applications or accessing shared network resources, without granting them full administrative control over the system.
</p>
<br />

<h2>Create additional users inside the organizational Units called EMPLOYEES with PowerShell script and attempt to log into client-1 with one of the users</h2>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, additional user accounts are created within the EMPLOYEES organizational unit using a PowerShell script, which automates the process of adding multiple users at once. After the users are created, one of them is selected to log into Client-1 to test the user’s ability to authenticate and access the machine. This step verifies that the new users can successfully log in to domain-joined devices and that their access rights and group memberships are correctly configured. It also ensures that the PowerShell script correctly applied the necessary attributes for the users in the EMPLOYEES OU
</p>
<br />
