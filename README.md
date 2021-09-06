# AWS Virtual Private Cloud (VPC)
## Internet Gateway
## Subnets
### Route Tables
#### Network Access Control List (NACLs)
##### Security Groups

![]()

- What is VPC
- AWS isolated virtual network<br>
It allows us to control virtual network environment including selection of your own IP address range, we can create multiple subnets within one VPC with specific network configuration. We can use both IPv4 and IPv6 for most resources. It provides security for your services or instances.

- What is an Internet Gateway?<br>
It can transfer communications between an enterprise network and the internet. It allows internet access into the VPC.

- What is a Subnet?<br>
It is a segmented piece of a larger network - the goal of a subnet is to split a large network into a group of smaller interconnected networks to help minimise traffic - or navigate traffic securely.

- Route Table<br>
It contains a set of rules (routes), that are used to determine where the network traffic from your subnet or gateway is directed.

- Network Access Control List (NACL)<br>
NACLs are stateless- we have to explicitly allow inbound and outbound rules - they are an added layer of security ay subnet level

### Step 1: create a VPC with IP valid CIDR block
`10.0.0.0/16` - `10.10.0.0/16`
### Step 2: Create internet gateway
2.1: Attach the IG to your VPC
### Step 3: Create route table
3.1: Edit route and instert your IG in `target`
### Step 4: Create public subnet
`10.0.1.0/24`<br>
4.1: Associate public subnet with our RT
### Step 5: Create public NACLs
Set inbound and outbound rules for this
### Step 6: Create a security group for our app