<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Install active directory domain services on the domain controller
- Create domain admin user within the domain
- Join client-1 to your created domain
- Setup remote desktop for non-administrative users on cleint-1
- Check connectivity by creating additional users and attempt to log in to client-1 with one of those users

<h2>Actions and Observations</h2>

<p>
<img src="https://i.imgur.com/otIwJ97.png">
</p>
<p>
Checking connectivity between two virtual machines first require setting up active directory in the domain controller. Active directory helps to organize network resources like users, computers, and services. It also provides authentication, authorization, and centralized management within a network, allowing administrators to control access and security policies.
</p>
<br />

<p>
<img src="https://i.imgur.com/xDCXPgz.png">
</p>
<p>
After domain controllers are are created and active directory intalled on them domain admin users needs to created. So this basically will be like tha ccount that handles the backend activities of active directory like assinging permissions, authorizing changes or access.
</p>
<br />

<p>
<img src="https://i.imgur.com/pHXA3LY.png">
</p>
<p>
This step has already been done but put here as a reiteration because without it active directory wouldn't function as it should and networking between the two virtual machine is futile.
</p>
<br />

<p>
<img src="https://i.imgur.com/3R6p7KS.png">
</p>
<p>
This step is important for the next step because it basically allows for domain users not only admin users be able to use remote desktop on the network and active directiry you have created.
</p>
<br />

<p>
<img src="https://i.imgur.com/zKxQ80v.png">
</p>
<p>
This final step is crucial because this is where you create domain users that you can assign permissions, authorization and access to which is basically your network.
</p>
<br />
