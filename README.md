<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Active Directory Installation & Configuration in Minutes!</h1>
In this lab, I started by installing Active Directory Domain Services on DC-1 and promoting it to a domain controller for the domain mydomain.com. Next, I created organizational units (OUs) for EMPLOYEES, ADMINS, and CLIENTS to help organize the domain structure. I then added a new employee to the Domain Admins group to grant the appropriate permissions. Afterward, I joined Client-1 to the domain and organized it within the CLIENTS OU. I configured access for non-administrative users to ensure proper permissions. Using PowerShell, I created additional users in the EMPLOYEES OU, and finally, I attempted to log into Client-1 with one of these new user accounts to verify that the setup was functioning as expected.<br />


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
<img src="https://i.imgur.com/BbRUCvW.jpeg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I installed Active Directory Domain Services (AD DS) on the DC-1 virtual machine and promoted it to a domain controller for the domain mydomain.com. Once promoted, DC-1 took on the responsibility of managing and storing the directory information for the domain. It now handles user authentication, authorization, and essential services like DNS for domain-joined computers. This process also configured the domain controller to support network management, security policies, and resource access for users and computers within the mydomain.com domain.
</p>
<br />

<h2>Create Organizational Units called EMPLOYEES, ADMINS and CLIENTS</h2>
<p>
<img src="https://i.imgur.com/xAol0u5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I created Organizational Units (OUs) within Active Directory, naming them EMPLOYEES, ADMINS, and CLIENTS. These OUs help logically organize and manage different groups of users and resources based on their roles or functions within the domain. For example, the EMPLOYEES OU includes regular staff members, the ADMINS OU contains administrative accounts with higher privileges, and the CLIENTS OU holds machines or users that need different access levels or management. Organizing resources into OUs simplifies administration, allows for the application of specific group policies, and makes it easier to delegate management tasks based on the role of each group.
</p>
<br />

<h2>Create a new employee named Jane Doe and add her to the Domain Admins Security Group</h2>
<p>
<img src="https://i.imgur.com/cZP3t8a.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I created a new user account for Jane Doe in Active Directory and added her to the Domain Admins Security Group. By assigning her to this group, I granted her full administrative privileges over the domain, allowing her to manage domain settings, users, and other resources across the network. This ensures that Jane has the necessary permissions to perform high-level administrative tasks within the domain, such as managing user accounts, group policies, and server configurations.
</p>
<br />

<h2>Login to Client-1 and join it to the domain</h2>
<p>
<img src="https://i.imgur.com/vLAbSxx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I logged into Client-1 and joined it to the mydomain.com domain by configuring its system settings to communicate with the domain controller. This action allowed Client-1 to become part of the domain, enabling it to use domain-based authentication, access network resources, and receive domain policies. By joining the domain, Client-1 can now be centrally managed through Active Directory, making administration and user access control within the network much easier.
</p>
<br />

<h2>Login to DC-1, verify Client-1 is Joined, and copy it into the organizational Units called CLIENTS</h2>
<p>
<img src="https://i.imgur.com/hhHkYhl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I logged into DC-1, the domain controller, and confirmed that Client-1 had been successfully joined to the mydomain.com domain by checking its status in Active Directory. After verifying its domain membership, I moved Client-1 into the CLIENTS organizational unit (OU), which helps organize and manage the client machine within the domain. Placing Client-1 in the CLIENTS OU ensures that it can inherit specific group policies and permissions designed for client devices, making it easier to manage access and apply configurations for that group.
</p>
<br />

<h2>Configure Client-1 so that non-administrative Users can access</h2>
<p>
<img src="https://i.imgur.com/wW6FgwP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I configured Client-1 to allow access for non-administrative users by modifying the machine's permissions, group memberships, and local user settings. This involved ensuring that users who are not part of the Administrators group could still log in and access the necessary resources while restricting access to sensitive administrative functions. By configuring these settings, I made sure that non-administrative users had the rights they needed to perform their tasks, such as running applications or accessing shared network resources, without granting them full administrative control over the system.
</p>
<br />

<h2>Create additional users inside the organizational Units called EMPLOYEES with PowerShell script and attempt to log into client-1 with one of the users</h2>
<p>
<img src="https://i.imgur.com/lLqF6cS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In this step, I used a PowerShell script to create additional user accounts within the EMPLOYEES organizational unit, automating the process of adding multiple users at once. After the users were created, I selected one of them to log into Client-1 and tested the user’s ability to authenticate and access the machine. This step helped verify that the new users could successfully log in to domain-joined devices and that their access rights and group memberships were correctly configured. It also ensured that the PowerShell script had correctly applied the necessary attributes for the users in the EMPLOYEES OU.
</p>
<br />
