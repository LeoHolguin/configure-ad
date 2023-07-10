<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Virtual Machins in Azure
- Remote Desktop Protocol and Installing Active Directory
- Finalizing Active Directory
  

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="319" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/67c73e0a-a70e-4a59-8bbb-ea100d686395">
<img width="428" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/272c3375-03ac-4006-a5d7-ede1499f05ee">

</p>
<p>
First, we are going to create two virtual machines in Azure. Our first VM is going to be a domain controller which we are going to install an active directory and the second VM is going to be a client. Now we are going into the network settings for DC-1 and changing its ip status to static.
</p>
<br />

<p>
<img width="306" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/23cfb389-7f6d-4b61-a2fd-1f75b45639e7">
<img width="953" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/0664d56a-0424-4817-bb8f-38847157d272">



</p>
<p>
Since we are on Windows, we are going to use the remote desktop protocol to connect to our virtual machines. Now we are firdt going to login to our Domain controller and install active directory. We are going to open service manager and click on a add roles and features, click next until you can check off active directory domain services, and click on install.
</p>s
<br />

<p>
<img width="421" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/e2ca7026-699c-4fc6-a0e3-aa9d5c086247">
<img width="575" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/162942ea-7818-4981-b9bf-1a333a5da665">



</p>
<p>
On the top right we are seeing a flag with a explanation point, click on it and to finalize installing active direcotry and turn the server into a domain controller. We are going to add a new forest with a the root name being mydomain.com and click intall when we are finish. Once its done install the computer is going to restart.
</p>
<br />
<p>
<img width="337" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/1c951edd-4bef-4081-a8ad-d16c8aceeff3">
<img width="410" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/a64801cc-ea94-4a9d-b25c-f336c9d9d1ae">
<img width="563" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/7d1383f4-443d-474f-84bf-c6931a4391fe">



</p>
<p>
Since we actaully changed this computetr to a domain controller we have to sign in by using the domain user we made. Finally, when we login to the domain controller we can check if we have succfeully intsalled active direcoty by going to service manager, click on tools and if we don everything right we should be able to see Active directoy user and computers. Perfect we installed active diretory and now if we want we can accounts and give them permissions.
</p>
<br />
