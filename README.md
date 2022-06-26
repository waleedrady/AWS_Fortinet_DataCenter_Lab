# AWS_Fortinet_DataCenter_Lab
Deployment script that allow you to deploy FortiGate, FortiManager, FortiAnalyzer, FortiSandbox, FortiAuthenticator and Latest Windows Server 2022 and Ubunutu


Source Code for this Module (https://github.com/WEEMR/terraform-aws-Fortinet_DataCenter_Lab)

Terraform Registery         (https://registry.terraform.io/modules/WEEMR/Fortinet_DataCenter_Lab/aws)

![image](https://user-images.githubusercontent.com/82145296/175827673-4915827e-0a9f-453e-b489-f86ebfd60e7c.png)

The module will create the below resources:

- 8 x VPCs for Three Hubs and 4 Spokes Topology.
- Networking Stack (VPC, Subnets, Route Tables, Security Groups, Internet Gateway and NAT Gateway[for FortiSandbox])
- 7 x FortiGate with 3 interfaces (Two Interfaces in two different Public Subnets [for SD-WAN testing] and one in the Private subnets)
- FortiManager       - [Behind Hub 1 LAN]
- FortiAnlayzer      - [Behind Hub 1 LAN]
- FortiAuthenticator - [Behind Hub 1 LAN]
- FortiSandbox       - [Seperate VPC \ Independent]
- 7 x Windows Server 2019 Behind each FGT Port 3 [LAN]
- 7 x Ubunutu Server with Apache installed, iperf, fzf, pydf, firefox, lynx and elinks installed on it behind each FGT port 3 [LAN]
- Route53 Public DNS Hosted Zone
- Route53 Health Checks for all the FortiGates IPs


// The DNS Hosted Zones must be sub-zones for a domain that is registered or managed by AWS Route53 //

// i.e xyz.com is the domain name and you will create the subzone Lab1.xyz.com // 
