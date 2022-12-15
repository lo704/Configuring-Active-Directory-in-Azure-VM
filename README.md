![AD1](https://user-images.githubusercontent.com/33810883/207665691-103a8c7d-8e5a-422e-b6ff-843855fb738f.png)
# Configuring Active Directory in Azure Virtual Network
This Project outlines the implementation and configuration of Microsoft Active Directory in Azure Virtual Network 

<h2>Environment and Technologies</h2>

- Microsoft Azure VMs(Compute Resources)
- Active Directory Domain Services
- Remote Desktop (RDP)
- PowerShell (Script)

<h2>Operating Systems</h2>

- Windows 10 (21H2)
- Windows Server (2022)

<h2>Configuration Setup</h2>

In this project, three VMs will be created in the same Virtual Network(VNet). Two client machines CL-1, CL-2 and a Domain Controller DC-1. The Domain Controller must have a static private IP as it will provide Active Directory Services to all the clients. Using RDP We will have control over the client machines, set the DNS configurations to join the Domain and use DC-1 as the virtual network DNS server.
