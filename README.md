# AWS-How-to-create-VPC-with-resources
Creating Networking Resources in an Amazon Virtual Private Cloud (VPC)

Create a VPC
Internet Gateway
Route Table 
Security Group
Network Access List
and EC2 instance to create a routable network within the VPC
Familiarize yourself with the console

A Virtual Private Cloud (VPC) is like a data center but in the cloud. Its logically isolated from other virtual networks from which you can spin up and launch your AWS resources within minutes.


<img width="1657" height="588" alt="Screenshot 2026-09-11 084412" src="https://github.com/user-attachments/assets/73f26e96-b404-4d11-84af-1627f2a62f01" />





*Create at VPC with a Public Subnet >> this VPC includes an IPv4 CIDR block

<img width="1917" height="1077" alt="Screenshot 2026-09-11 085601" src="https://github.com/user-attachments/assets/7b1c3468-1287-4a2b-8771-3e56cd947aeb" />

*Adding a subnet to be associated with the VPC
<img width="1917" height="892" alt="Screenshot 2026-09-11 090006" src="https://github.com/user-attachments/assets/60064510-e606-421c-9765-3664cebdec78" />


*Adding route table for our traffic withiin the VPC

<img width="1917" height="1077" alt="Screenshot 2026-09-11 090535" src="https://github.com/user-attachments/assets/b99c7441-b2f9-4e85-8478-5b0b2a7a6098" />



*Create Internet Gateway and attach Internet Gateway

<img width="1917" height="1077" alt="Screenshot 2026-09-11 091120" src="https://github.com/user-attachments/assets/37d5eafe-5365-429c-a91b-ff5c1fa47581" />


*Add route to route table and associate subnet to route table
>>>In the Destination we have 0.0.0.0/0  This is the for our traffic route to the IGW. We are telling the route table that any traffic that needs internet connection will use 0.0.0.0/0 to reach the IGW so that it can reach the internet.

*Creating a Network ACL Access Control List
<img width="1917" height="1077" alt="Screenshot 2026-09-11 091120" src="https://github.com/user-attachments/assets/3eec7499-734e-40c1-91f5-ceb9e441f036" />

>>> With a Public Subnet,rules for the traffic inccluding inbound and outbound

*Creating a Security Group

<img width="1917" height="1077" alt="Screenshot 2026-09-11 091842" src="https://github.com/user-attachments/assets/75818c88-50e5-4f7d-ad76-f2615ec05b4e" />

>>>security group is a virtual firewall at the instance level that controls inbound and outbound traffic. Just like a NACL, security groups control traffic; however, security groups cannot deny traffic. Security groups are stateful; you must allow traffic through the security group as it blocks everything by default, and it must be associated to an instance. A security group has the following parts for both inbound and outbound rules:

<img width="1917" height="1077" alt="Screenshot 2026-09-11 092148" src="https://github.com/user-attachments/assets/14bdc2fb-adde-4638-ac1f-b7600891adea" />

Inbound Source: It can be an IP or a specific resource
Outbound Destination: Can by an IP such as anywhere (0.0.0.0/0)
Protocol: Example UDP or TCP
Port range: All or specific range
Description: You can input a description


<img width="1917" height="1077" alt="Screenshot 2026-09-11 092845" src="https://github.com/user-attachments/assets/86735954-1b5d-48d7-ab0b-2e2c82d07cdc" />

* Launching an EC2 instance within our Public subnet and test connectivity by running the command ping

<img width="1917" height="1077" alt="Screenshot 2026-09-11 093904" src="https://github.com/user-attachments/assets/0a5e559f-0592-4dc4-9da4-ce3a5ace2ef8" />


>>> Instance launch > Amazon Linux > AWM AMI 2023 > KEYPAIR > Network witH VPC , plublic subnet and firewall created in security groups .

<img width="1917" height="1078" alt="Screenshot 2026-09-11 094716" src="https://github.com/user-attachments/assets/309e5efc-0687-4eb8-92b5-66e93d5040ec" />

* PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!

  ping google.com






  The END!!!
