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

*Create at VPC with a Public Subnet >> this VPC includes an IPv4 CIDR block

*Adding a subnet to be associated with the VPC

*Adding route table for our traffic withiin the VPC

*Create Internet Gateway and attach Internet Gateway

*Add route to route table and associate subnet to route table
>>>In the Destination we have 0.0.0.0/0  This is the for our traffic route to the IGW. We are telling the route table that any traffic that needs internet connection will use 0.0.0.0/0 to reach the IGW so that it can reach the internet.

*Creating a Network ACL Access Control List
>>> With a Public Subnet,rules for the traffic inccluding inbound and outbound

*Creating a Security Group
>>>security group is a virtual firewall at the instance level that controls inbound and outbound traffic. Just like a NACL, security groups control traffic; however, security groups cannot deny traffic. Security groups are stateful; you must allow traffic through the security group as it blocks everything by default, and it must be associated to an instance. A security group has the following parts for both inbound and outbound rules:

Inbound Source: It can be an IP or a specific resource
Outbound Destination: Can by an IP such as anywhere (0.0.0.0/0)
Protocol: Example UDP or TCP
Port range: All or specific range
Description: You can input a description

* Launching an EC2 instance within our Public subnet and test connectivity by running the command ping
>>> Instance launch > Amazon Linux > AWM AMI 2023 > KEYPAIR > Network witH VPC , plublic subnet and firewall created in security groups .


* PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!  PING!!!

  ping google.com






  The END!!!
