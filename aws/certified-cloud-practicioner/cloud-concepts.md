# Cloud Concepts

## Before AWS

Before AWS & Cloud computing came into picture everthing was static i.e. you need to plan your users beforehand, wait for the long process of procurement, configuring, testing the servers before rolling it out in prod. This resulted in underprovisioning or overprovisioning, resulting either in loss of customers or waste of money.

This was no way scalable for spike traffic (eg. Big Billion Days sale in Flipkart)

## After AWS

After AWS everything was disposable and temporary, machines came up in seconds, computing became "Elastic" & efficiency and agility were now available with infrastructure.

## Agility

With AWS came agility. These are the 3 factors that define agility in Cloud:

- Speed
- Experimentation
- Culture of Innovation

### Speed

You can go global in seconds. Faster provisioning of resources.

### Experimentation

You can now have your infrastructure as Code (the reason why Puppet, Ansible, Terraform, Chef, SaltStack exist). You can safely experiment with new features & configs (Blue/Green deployments, CI/CD, environment separation etc.) Infra is now templated! (eg. AWS CloudFormation, Terraform)

### Innovation

With experimentation, you can innovate more without worrying about risks/costs more often.

## The Global Infra of AWS

There are 3 terms revolving around the global infra of AWS:

- Regions
- Availability Zones (AZs)
- Edge Locations

The main purpose of this level of redundancy is to have a fault-tolerant (Operational even after some component fails) & highly available (Always available with reduced downtime & automated) infra.

### Regions

This is a physical location in the world. This can have multiple AZs.

### AZ

This is a datacentre in a region. Note that a single AZ can be constituted of multiple datacentres, separated by a few kilometres. When you have 2 or more AZs, you have a region.

### Edge locations

This is basically a Content Delivery Network (CDN) point for the region. They are a lot more than the AZs. They serve a purpose of caching the content so the audience in the region can have the content at a very low latency.

## Elasticity

You can scale up/down the resources with a few clicks resulting in faster deployment of applications, pay only for what's used and save money, take your time to use services, adapt to consumption, new management strategies, new launches of products.

## Security & Compliance

Customer retains control over which region the data is located. This is because there can be regional data compliance requirements. Before AWS, the audits would be long & expensive. AWS provides governance capabilites for monitoring & taking actions. They also provide industry-leading capabilites that pass the strictest compliance requirements.



[Next](core-services.md)