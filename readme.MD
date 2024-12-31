# Terraform aws vpc module customised
This module is going to create the following resources.
for high availability we are going to get first 2 AZ's.

*vpc
*Internet gateway associated with vpc
* 2 public subnets
* 2 private subnets
* 2 database subnetes
* database subnet group
* 1 elastick ip
* 1 NAT gateway
* public route table
* private route table
* databse route table
* routees
* route atble associtation with subnets
* pering with default vpc if required
* perring routs in accepter and requester route tables

#Inputs
project_name (mandatory) : user must supply  
environment (mandatory) : user must supply  
vpc_cidr (mandatory) : user must suppty ther vpc cidr
enable_dns_hostnames (optional ) : defaults to true.
common_tags (optional ) : default is empty . user can supplt tags in list of string
vpc_tags (optional) : default is empty . user can supplt tags in list of string
igw_tags (optional) :default is empty . user can supplt tags in list of string
public_subnet_cidrs (mandatory) : user must supply ONLY 2 cidrs
public_subnet_tags (optional) : default is empty . user can supplt tags in list of string
private_subnet_cidrs (mandatory) : user must supply ONLY 2 cidrs
private_subnet_tags (optional) : default is empty . user can supplt tags in list of string
database_subnet_cidrs (mandatory) : user must supply ONLY 2 cidrs
database_subnet_tags (optional) : default is empty . user can supplt tags in list of string
db_subnet_group_tags ( optional) :  default is empty . user can supplt tags in list of string
nat_gateway_tags ( optional) :  default is empty . user can supplt tags in list of string
public_route_table_tags ( optional) :  default is empty . user can supplt tags in list of string
private_route_table_tags ( optional) :  default is empty . user can supplt tags in list of string
database_route_table_tags ( optional) :  default is empty . user can supplt tags in list of string
is_peering_required (optional) : DEFAULTS to False
vpc_peering_tags ( optional) :  default is empty . user can supplt tags in list of string

#outputs
vpc_id : vpc id created
public_subnet_ids :  list of 2 public subnet ids created
private_subnet_ids :  list of 2 priavte subnet ids created
database_subnet_ids :  list of 2 database subnet ids created
