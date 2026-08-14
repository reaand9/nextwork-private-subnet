<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](http://nextwork.ai/projects/aws-networks-private)

**Author:** Andrea Virador  
**Email:** venicevirador@gmail.com

---

## Creating a Private Subnet

![Image](http://nextwork.ai/zealous_azure_proud_blackberry/uploads/aws-networks-private_afe1fdbd)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC (Virtual Private Cloud) is a service that lets you launch AWS resources, like virtual servers and databases, inside a private and isolated virtual network that you define and control. It acts as your own secure data center in the cloud.

### How I used Amazon VPC in this project

I used Amazon VPC to create and configure a private network environment in AWS. I created a VPC with the CIDR block 10.0.0.0/16, along with subnets, an internet gateway, route table, security group, and network ACLs to control network traffic and connectivity within the VPC.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is how easy it is for hackers to get into your resources if you don't set up rules and security correctly.

### This project took me...

This project took me 30 mins.

---

## Private vs Public Subnets

Public subnets are directly connected to the internet, allowing seamless access through an internet gateway. In contrast, private subnets operate exclusively within the Virtual Private Cloud (VPC), ensuring enhanced security and isolation.

Having private subnets are useful because there may be data or resources that we want to keep private and secured.

My private and public subnets cannot share the same IP address allocation.

![Image](http://nextwork.ai/zealous_azure_proud_blackberry/uploads/aws-networks-private_afe1fdbd)

---

## A dedicated route table

By default, my private subnet is associated with my public route table.

I had to set up a new route table because I want to keep my private and public route instructions separate since the existing public route table has a connection to the internet. 

My private subnet's dedicated route table only has one inbound and one outbound rule that allows local routes only.

![Image](http://nextwork.ai/zealous_azure_proud_blackberry/uploads/aws-networks-private_b4b904b5)

---

## A new network ACL

By default, my private subnet is associated with the public  NACL

I set up a dedicated network ACL for my private subnet to keep my data secure.

My new network ACL has two simple rules - to deny both inbound and outbound traffic.

![Image](http://nextwork.ai/zealous_azure_proud_blackberry/uploads/aws-networks-private_1ed2cb07)

---

---
