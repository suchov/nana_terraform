# Terraform learning with Nana

https://www.udemy.com/course/draft/3795590/learn/lecture/24588360#overview

The course is out of avaliability and Nana deleted the gitlab part, shit...

https://gitlab.com/suchov/udemy-terraform-learn - the copy I did and it was quite a smart
move.

And installing the AWS Command Line Interface

## Terraform Providers

https://registry.terraform.io/browse/providers

AWS one's
https://registry.terraform.io/providers/hashicorp/aws/latest

## AWS resources

VPC, Subnet

Virtual Private Connection - page on AWS and your own private network in the cloud.
VPC spans all avaliability zones in that region.
You can have multiple VPC's in different Regions.
Virtual representation of network infrastructure.
Set up the router, do all the network configuration, firewall...
All this physical network infra moved in cloud.

Subnets - sub networks.(avaliability zones in your VPC)
Like a private network inside a network.
Private and public subnets in VPC exists.
You choose private or public subnets by blocking or not outside traffic to the subnet.
But other services inside the VPC will have access!
Public subnet - for example you have your 8000 port open to get the inernet traffic in/out.
And your web app can talk to other subnet that is private(connect to the DB, ...)
Internal IP addresses will be given to you from the range that is specified.
Private ip address defined on VPC level and each subnet get it's own range from the total
range.
Internet Gateways - the component that allows external traffic in AWS.

Controlling Access
- Secure your components
- Control access to you VPC
- Control access to your individual server instances
(basically a firewall configuration)

That security control can be controled on multiple levels in VPC.
AWS makes it pretty flexible and granular, how it can be done.
In many cases you don't need some advanced network configs.
Network ACLs firewall rules for subnets.
Seciruty groups - firewalls on virtual machine level.

## Creating AWS resources using provider
