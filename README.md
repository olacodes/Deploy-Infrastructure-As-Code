## Deploy a high-availability web app using CloudFormation

This project deploys a simple high-availability, high-security web app using CloudFormation to Amazon Web Service AWS.

### Infrastructure Diagram

![Infrastructure Diagram](/assets/Deploy-WebApp-Cloudformation.png)

### AWS Services Harnessed

- [AWS CloudFormation](https://aws.amazon.com/cloudformation/):AWS CloudFormation lets you model, provision, and manage AWS and third-party resources by treating infrastructure as code.

- [Amazon Elastic Compute Cloud (Amazon EC2)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html): Amazon Elastic Compute Cloud Provides scalable computing capacity in the Amazon Web Services (AWS) Cloud

- [Amazon Elastic Block Storage (Amazon EBS)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html): Amazon Elastic Block Store (Amazon EBS) provides block level storage volumes for use with EC2 instances

- [Amazon Elastic Load Balancer (ELB)](https://aws.amazon.com/elasticloadbalancing/): Amazon Elastic Load Balancer automatically distributes incoming application traffic across multiple targets and virtual appliances in one or more Availability Zones (AZs).

- [Amazon Virtual Private Cloud (VPC)](https://docs.aws.amazon.com/vpc/latest/userguide/what-is-amazon-vpc.html): Amazon Virtual Private Cloud (Amazon VPC) enables you to launch AWS resources into a virtual network that you've defined

- [Internet Gateway](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Internet_Gateway.html): An internet gateway is a horizontally scaled, redundant, and highly available VPC component that allows communication between your VPC and the internet

- [NAT Gateways](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-nat-gateway.html): A NAT gateway is a Network Address Translation (NAT) service

- [Routing Table](https://docs.aws.amazon.com/vpc/latest/userguide/VPC_Route_Tables.html): A route table contains a set of rules, called routes, that determine where network traffic from your subnet or gateway is directed.

### Project Description

This project contains 2 bash script, 2 yaml files and 2 json files.

The Bash Scripts is a convenient scripts to create and update stack passing file parameters, they are:

- create.sh: To create Stack
- update.sh: To update stack

The YML files are networks and server provisioning file, they are:

- udadagram-network.yml: Contains all networks services like VPC, subnets etc
- udagram-server.yml: Contains all AWS services like EC2, EBS, ELB etc

The JSON files are parameters file for both the network and the server.

### Usage

Using the cloud formation scripts in this project is very simple, all you need is to configure your AWS locally and run the following commands:

#### To create the networks and Servers:

   1. `./create.sh udagram-network udagram-network.yml udagram-network-parameters.json`
   2. `./create.sh udagram-server  udagram-server.yml udagram-server-parameters.json`

#### To update networks and Servers:

   1. `./update.sh udagram-network udagram-network.yml udagram-network-parameters.json`
   2. `./update.sh udagram-server  udagram-server.yml udagram-server-parameters.json`


### Author

Sodiq Olatunde