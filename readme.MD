# custum AWS VPC Module

![alt text](images/vpc.jpg)

This module is developed for joindevops.com.We are creating following resources. This module creates resoures in first 2 Availibility Zone AZ for high availability HA.

* VPC
* Internet gateway
* Internet and VPC attachment
* 2 Public subnets. 
* 2 Private subnets
* 2 database subnets
* EIP
* NAT gateway
* Public Route table
* Private Route table
* database Route table
* Route table and subnet associations
* Routes in all tables
* peering if required for user
* Routes of peering in requestor and acceptor VPC. 
* database subnet group

### Inputs

* Project_name (Required): user should mention project name. Type is string
* environment (optional): Default value is dev. Type is string.
* Common_tags (Required): user should provide their tags related to their project. Type is map
* vpc_cidr (optional): defaultvalue is 10.0.0.0/16. Type is string.
* enable_dns_hostnames (optional): Default value is true.type is Bool.
* vpc_tags (optional): Default value is empty. Type is map.
* igw_tags (optional): Default value is empty. Type is map.
* public_subnet_cidrs (Required): User has to provide 2 valid subnet CIDR. 
* public_subnet_cidr_tags (optional): Default value is empty. Type is map.
* private_subnet_cidrs (Required): User has to provide 2 valid subnet CIDR. 
* private_subnet_cidr_tags (optional): Default value is empty. Type is map.
* database_subnet_cidrs (Required): User has to provide 2 valid subnet CIDR. 
* database_subnet_cidr_tags (optional): Default value is empty. Type is map.
* database_subnet_group_tags(optional): Default value is empty. Type is map.
* nat_gateway_tags(optional):  Default value is empty. Type is map.
* public_route_table_tags (optional):  Default value is empty. Type is map.
* private_route_table_tags (optional):  Default value is empty. Type is map.
* database_route_table_tags (optional):  Default value is empty. Type is map.
* is_peering_required (optional): Default value is false. Type is Bool.
* acceptor_vpc_id (optional): Default value is empty. default VPC ID would be taken. type is string.
* vpc_peering_tags (optional):  Default value is empty. Type is map.


### Outputs 

* vpc_id: VPC ID
* public_subnet_ids: A list of 2 public IDS created.
* private_subnet_ids: A list of 2 private IDS created.
* database_subnet_ids: A list of 2 database IDS created.
* atabase_subnet_group_id: A database subnet group ID created.