# Core AWS Services

AWS provides a ton of services (and are growing). AWS has some services which can be classified as "core" because these are what power the other services, which in one form or other are abstracted away from user at a certain level.

These core services are:

- EC2 (Elastic Cloud Compute) (Compute)
- Lambda (Serverless Computing) (Compute)
- EC2 Auto Scaling (Compute)
- Elastic Beanstalk (Computing without management) (Compute)
- ELB (Elastic Load Balancer) (Compute)
- ALB (Application Load Balancer) (Compute)
- S3 (Simple Storage Service) (Storage)
- EBS (Elastic Block Store) (Storage)
- Glacier (Archival Service) (Storage)
- IAM (Identity & Access Management) (Security)
- VPC (Virtual Private Cloud) (Networking)
- RDS (Relational Database Service) (Database)
- DynamoDB (noSQL Database Service) (Database)
- Aurora (Database Engine for AWS) (Database)
- Amazon Redshift (Data Warehousing & ETL Service) (Database & Analytics)

## AWS Service Categories

AWS provides a lot of services for a variety of domains like game development, VR development, Business Analytics etc. Hence, their services are divided into categories. They are (Those check marked are important for exam):

- [X] Compute
- [X] Storage
- [X] Networking
- [X] Security, Identity & Compliance
- [X] Databases
- [ ] Migration
- [ ] Developer Tools
- [ ] Management Tools
- [ ] Analytics
- [ ] Artificial Intelligence
- [ ] Mobile Services
- [ ] Application Services
- [ ] Messaging
- [ ] Business Productivity
- [ ] Desktop & App Streaming
- [ ] Internet of Things
- [ ] Contact Center
- [ ] Game Development

## AWS Global Infrastructure

There are 3 terms revolving around the global infra of AWS:

- Regions
- Availability Zones (AZs)
- Edge Locations

The main purpose of this level of redundancy is to have a fault-tolerant (Operational even after some component fails) & highly available (Always available with reduced downtime & automated) infra.

### Regions

This is a physical location in the world. This can have multiple AZs. Data in one region DOES NOT get replicated to other regions.

### AZ

This is a collection of datacentres in a region. Note that a single AZ can be constituted of multiple datacentres, separated by a few kilometres, connected with low latency link. When you have 2 or more AZs, you have a region.

### Edge locations

This is basically a Content Delivery Network (CDN) point for the region. They are a lot more than the AZs. They serve a purpose of caching the content so the audience in the region can have the content at a very low latency.

## Virtual Private Cloud (VPC)

AWS Offers a variety of services in compute, storage, network, databases, application services etc. These resources are needed to be accessed via the IP protocols. Customers need to adhere to networking requirements for creating a compliant and secure cloud. Amazon VPC offers a logical separation & isolation of the resources through networking. It is a networking service for providing networking capabilites to customers.

It is a private network in the cloud, using same concepts as on-prem networking. You have complete control over the configuration. It offers several layers of security controls (eg. subnets, Network ACLs (NACL), custom route tables)to allow/deny specific internal & internet traffic. Other AWS services also deploy in VPC (eg. RDS, EC2, ELB etc.)

**Features of VPC:**

- This is built upon the high availability of AWS Regions & AZs.
  - A VPC lives within a region
  - Multiple VPCs per account (actual no. is 5, which is a soft limit)

- Subnets which are used to divide VPC and allowing VPC to span to multiple AZs (soft limit of subnets is 200)

- Route tables for controlling traffic outside of subnets.

- Internet Gateway (IGW) for allowing Internet access from VPC.

- NAT gateway for allowing private subnet resources to access Internet.

- NACLs for controlling access to subnets and it is stateless.