# Lab 2: Build a VPC and Launch a Web Server

Hands-on AWS networking lab. I build a custom Amazon VPC with public and private subnets across two Availability Zones, control traffic with route tables and a security group, and launch a web server on Amazon EC2. Region: US East (N. Virginia).

## What I'm building

| Resource | Details |
|----------|---------|
| VPC | `lab-vpc`, CIDR `10.0.0.0/16` |
| Public subnet 1 | `10.0.0.0/24`, Availability Zone A |
| Private subnet 1 | `10.0.1.0/24`, Availability Zone A |
| Public subnet 2 | `10.0.2.0/24`, Availability Zone B |
| Private subnet 2 | `10.0.3.0/24`, Availability Zone B |
| Internet gateway | Lets the public subnets reach the internet |
| NAT gateway | In public subnet 1; lets private subnets reach the internet without being reachable from it |
| Public route table | `10.0.0.0/16` → local, `0.0.0.0/0` → internet gateway |
| Private route table | `10.0.0.0/16` → local, `0.0.0.0/0` → NAT gateway |
| Security group | Allows HTTP to the web server |
| EC2 instance | Web Server 1, in public subnet 2 |

## Progress

| # | Step | Screenshot |
|---|------|------------|
