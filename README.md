<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Creating a Private Subnet

**Project Link:** [View Project](https://nextwork.ai/projects/4e96e29d-98b8-551e-ae93-da39c36e30fd)

**Author:** Ahmed Umar Rehman  
**Email:** ahmedumar475@gmail.com

---

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_afe1fdbd)

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC is a logically isolated virtual network in AWS. It is useful because it allows me to control my resources, networking, and security.

### How I used Amazon VPC in this project

In today's project, I used Amazon VPC to create and configure public and private subnets with routing and network security controls.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project is how many separate networking components are needed to properly configure a private subnet.

### This project took me...

This project took me 30 mins

## Private vs Public Subnets

The difference between public and private subnets is that a public subnet has a route to an Internet Gateway, while a private subnet does not have a direct route to the Internet Gateway.

Having private subnets are useful because they keep resources isolated from direct internet access, improving security and reducing exposure to external threats.

My private and public subnets cannot have the same CIDR block because subnet IP ranges within a VPC cannot overlap.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_afe1fdbd)

## A dedicated route table

By default, my private subnet is associated with 10.0.2.0/24

I had to set up a new route table because the private subnet needs its own routing rules separate from the public subnet.

My private subnet's dedicated route table only has one inbound and one outbound rule that allows local traffic within the VPC.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_b4b904b5)

## A new network ACL

By default, my private subnet is associated with the default Network AC 0.0.0.0/0

I set up a dedicated network ACL for my private subnet because it allows me to define specific traffic rules for that subnet.

My new network ACL has two simple rules — one to allow inbound traffic and one to allow outbound traffic.

![Image](https://nextwork.ai/calm_indigo_beautiful_lizard/uploads/4e96e29d-98b8-551e-ae93-da39c36e30fd_1ed2cb07)

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/4e96e29d-98b8-551e-ae93-da39c36e30fd)*
