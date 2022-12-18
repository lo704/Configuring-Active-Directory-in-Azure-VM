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

In this project, three virtual machines (VMs) will be created in the same Virtual Network(VNet). Two client machines CL-1, CL-2 and a Domain Controller DC-1. The Domain Controller needs a static private IP address as it will be used to provide Active Directory Services to all clients. Using RDP We will have control over the client machines, set the DNS configurations to join the Domain and use DC-1 as the virtual network DNS server.

![ADS_Azure](https://user-images.githubusercontent.com/33810883/208271238-b8f3a99f-a3f8-430f-95bf-47ee0522d6a9.png)

<h2>Configuration Steps</h2>

1. Once All VMs are created in Azure, Change DC-1 network interface Private IP address settings default from to Dynamic to Static:

![Step1_DC-StaticIP](https://user-images.githubusercontent.com/33810883/208269998-892ff68c-8476-4f23-bf1f-3bf109f12d10.png)

2. Confirm all clients are able to communicate with the Domain Controller DC-1. To do this we will need to enable ICMPv4 (Core Networking Diagnostics) in DC-1 firewall settings located in Windows Defender Firewall and Advance Security by changinng the Inbound and Outbound Rules. Then using the commandline ping DC-1 private IP address from CL-1 and CL-2: 
![Step2_ICMPv4-Enable](https://user-images.githubusercontent.com/33810883/208276069-715273e0-1d24-4b29-876a-91b9c43336a1.png)

3.
4.
5.
