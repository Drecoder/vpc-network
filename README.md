# vpc-network
# AWS VPC Network Diagram

This repository provides a simple AWS VPC network layout, ideal for mid-level cloud engineers looking for a clear example of a basic two-tier architecture.

## Architecture Overview

The setup demonstrates a **two-tier architecture** with public and private subnets, including connectivity and security components.  

### Components

- **VPC**: Single Virtual Private Cloud encapsulating all resources.
- **Public Subnet**: Contains an EC2 instance accessible from the internet.
- **Private Subnet**: Contains an EC2 instance not directly accessible from the internet; outbound traffic is routed via NAT Gateway.
- **Internet Gateway (IGW)**: Enables internet access for resources in the public subnet.
- **NAT Gateway**: Provides secure internet access for private subnet instances.
- **Route Tables**:
  - Public Route Table: Routes `0.0.0.0/0` traffic through the IGW.
  - Private Route Table: Routes `0.0.0.0/0` traffic through the NAT Gateway.
- **Security Groups**:
  - Public EC2: Typically allows HTTP/HTTPS and SSH from trusted IPs.
  - Private EC2: Restricts access to connections from the public subnet or specific IP ranges.

## Diagram
![alt text](vpc-net.png)

## Purpose

This diagram serves as a **visual reference** for understanding how:
- Public and private subnets connect to the internet
- Private subnets securely access the internet via NAT
- Subnets communicate with each other
- Security Groups and route tables manage traffic flow

## Usage

Use this repository as a reference when designing or reviewing basic AWS VPC architectures. It can also be used as a starting point for more complex multi-tier networks.  

