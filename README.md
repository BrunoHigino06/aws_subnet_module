# Subnet Module

Whats is the subnet module? 
This module creates subnets.

How to use the subnets module? 
This module was created with list of strings to use for specification of the subnet parameters.

outputs:

subnet_ids : id of the created subnets
subnet_cidrblocks : cidr_block of the created subnets

To use this kind of variable in the module it's necessary create a instance of the variable on de main.tf, for example:

module "subnet" {<br>
  source = "git::https://github.com/BrunoHigino06/aws_subnet_module.git"<br>
<br>
  subnets_names      = ["subnet1", "subnet2"]<br>
  subnets_cidr_block = ["10.0.1.0/24", "10.0.2.0/24"]<br>
  subnet_az          = ["us-east-1a", "us-east-1b"]<br>
}
