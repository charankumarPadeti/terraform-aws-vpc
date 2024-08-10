### AWS VPC Module

This module creates following resources. We are getting first 2 AZ automatically.
* VPC
* Internet Gateway with VPC association
* 2 Public subnets in 1a and 1b
* 2 private subnets in 1a and 1b
* 2 Database subnets in 1a and 1b
* Elastic IP
* NAT gateway in a 1a subnet
* Public Route Table
* Private Route Table
* Database Route Table
* Subnets and route table associations
* VPC peering if user request
* Adding the peering route in default VPC , if user don't provide acceptor VPC explicitly.
* Adding the peering routes in public , private and database route tables.

### Inputs

* project_name (Required) - your project name
* environment (Required) - which environment you working in
* vpc_cidr (Optional) - Default value is 10.0.0.0/16 , user can override
* enable_dns_hostnames (Optional) - Default value is true
* common_tags (Optional) - Better to provide
* vpc_tags (Optional) - Better to provide
* igw_tags (Optional) - Deafult value is empty. type is map
* public_subnets_cidr (Required) - user must provide 2 valid subnets CIDR
* public_subnet_tags (Optional) - Deafult value is empty. type is map
* private_subnets_cidr (Required) - user must provide 2 valid subnets CIDR
* private_subnet_tags (Optional) - Deafult value is empty. type is map
* database_subnets_cidr (Required) - user must provide 2 valid subnets CIDR
* database_subnet_tags (Optional) - Deafult value is empty. type is map
* nat_gwy_tags (Optional) - Deafult value is empty. type is map
* public_route_table_tags (Optional) - Deafult value is empty. type is map
* private_route_table_tags (Optinal) - Deafult value is empty. type is map
* route_table_tags - (Optional)- Deafult value is empty. type is map
* is_peering_required (Optional) - Default value is false
* acceptor_vpc_id (Optional) - default value is default VPC ID
* peering_tags (Optional) - Deafult value is empty. type is map

### Outputs

* vpc_id - VPC ID created
* public_subnets_ids - 2 Public subnet ID created
* public_subnets_ids - 2 Private subnet ID created
* database_subnets_ids - 2 Database subnet ID created