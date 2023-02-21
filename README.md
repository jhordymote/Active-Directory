# Active-Directory
<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Setup Resources in Azure
- Set Domain Controller’s NIC Private IP address to be static
- Ensure Connectivity between the client and Domain Controller
- Install Active Directory and Create an Admin and Normal User Account in AD
- Join Client-1 to your domain
- Setup Remote Desktop for non-administrative
- create bunch additiona; users and run the script.


<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/xzdIFEo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create Ressource and both virtual machine which all the steps are in the first link, after creationg a Virtual Machine we will go pin our NIC (Network Interface) to the static status instead of dynamic (static status means IP will not change during lab) and this have to be done in your virtual machine and not the client. then we will get client IPaddress to remote it, make sure to remember all the set up when you were creating Ressource Groups because username and password will be need to login into Remote Desktop Connection.
<br />

<p>
<img src="https://i.imgur.com/DgUL1rk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After login in the client computer, from the command we will see you will see the connection is not working by pinging the IPaddress, Then go back to the virtual machine to get your IPaddress and login to the remote desktop connection, so you can have both machine open, than step up or allow some program that block ping client machine, then after you will notice the ping it is working. 
</p>
<br />

<p>
<img src="https://i.imgur.com/OphR9zL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From your computer you can open server manager, install Active Directory and turn server to a Domain Control. creating domain controle with domain name and password whihc we will help to login. ( after steup domain, the remote will logoff and ask to reconnect, in this time we will not need our virtual machine logins intead we will use domain login because we turn computer to the domain's one)
</p>
<br />

<p>
<img src="https://i.imgur.com/C1mrKzP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We can create bunch of additional users which as administrators can assign them with or without limit of file's access in the company or for own safety, and with this a lead administrator have capability to delete someone's account or reset password.and to have this access wehave to set the computer to a domain control in DNS to be able to work
</p>
<br />

<p>
<img src="https://i.imgur.com/RGSRbZv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
As administrator you will be allow and access any account indeed fix if something going on or he cannot connect.
</p>
<br />
