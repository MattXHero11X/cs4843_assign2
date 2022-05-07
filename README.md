# Matthew Herrada (mdf827) cs 4843 Cloud Coputing
Cloud Formation Web Server Documentation
__________

## Requirements
- network.yml creates subnets
- database.yml creates EC2 for database
- server.yml creates load balanced servers
__________
## Details
These YAMLs are used as creation templates for infrastrucure components of the webserver

- **network.yml**: A VPC of 2 private and public subnets, each attached to a NAT internet Gateway. As well as route tables for all subnets which are seto f rules to determine where data packets traveling over the internet travels to.
- **database.yml**: An EC2 instance with a VPC in a security group having private subnets, unable to access the internet directly.
- **server.yml**: A loadbalancer and scaling group, a group of of EC2 instances that share similar configurations. The scaling policy will power down the servers when idle, and have subnet groups with an inbound and outbound traffic policies.

