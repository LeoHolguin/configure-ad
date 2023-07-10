<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />



- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services


<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Creating Virtual Machins in Azure
- Use Remote Desktop Protocol and Installing Active Directory
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
Since we are on Windows, we are going to use the remote desktop protocol to connect to our virtual machines. Now we are first going to log in to our Domain controller and install the active directory. We are going to open service manager and click on add roles and features, click next until you can check off active directory domain services, and click on install.
</p>
<br />

<p>
<img width="421" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/e2ca7026-699c-4fc6-a0e3-aa9d5c086247">
<img width="575" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/162942ea-7818-4981-b9bf-1a333a5da665">



</p>
<p>
On the top right we are seeing a flag with an exclamation point, click on it to finalize installing our active directory and turn the server into a domain controller. We are going to add a new forest with the root name mydomain.com and click install when we are finished. Once it's done install the computer is going to restart.
</p>
<br />
<p>
<img width="337" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/1c951edd-4bef-4081-a8ad-d16c8aceeff3">
<img width="410" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/a64801cc-ea94-4a9d-b25c-f336c9d9d1ae">
<img width="563" alt="image" src="https://github.com/LeoHolguin/configure-ad/assets/138087728/7d1383f4-443d-474f-84bf-c6931a4391fe">



</p>
<p>
Since we changed this computer to a domain controller we have to sign in by using the domain user we made. Finally, when we log in to the domain controller we can check if we have successfully installed the active directory by going to the service manager, clicking on tools and if we have done everything right we should be able to see the Active directory user and computers. Congrats we successfully installed active directory and now if we want, we can create accounts and give them permissions.
</p>
<br />
