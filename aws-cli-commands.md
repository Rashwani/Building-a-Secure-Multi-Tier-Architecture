## Using the VPC Console, record the following:
##      VPC ID of Default VPC
##      Subnet ID of any subnet in the Default VPC -- this will be your public subnet


## Create a private subnet in us-east-1a
aws ec2 create-subnet --vpc-id ******** --cidr-block 172.31.96.0/20 --availability-zone us-east-1a --tag-specifications 'ResourceType=subnet,Tags=[{Key=Name,Value=private-1a}]'
## Save the SubnetID

## Create a private subnet in us-east-1b
aws ec2 create-subnet --vpc-id ******** --cidr-block 172.31.112.0/20 --availability-zone us-east-1b --tag-specifications 'ResourceType=subnet,Tags=[{Key=Name,Value=private-1b}]'
## Save the SubnetID

## Create a route table in the default VPC
aws ec2 create-route-table --vpc-id ******** --tag-specifications 'ResourceType=route-table,Tags=[{Key=Name,Value=PrivateRT}]'
## Save the RouteTableID   

## Associate BOTH subnets to the route table
aws ec2 associate-route-table --route-table-id ******** --subnet-id ********
aws ec2 associate-route-table --route-table-id ******** --subnet-id ********

## Create an Elastic IP
aws ec2 allocate-address
## Save the AllocationID  



## Create a NAT gateway
aws ec2 create-nat-gateway --subnet-id ******** --allocation-id eipalloc-********
## Save the NATGatewayID  

## Update the private route table to point to the NAT gateway
aws ec2 create-route --route-table-id ******** --destination-cidr-block 0.0.0.0/0 --nat-gateway-id ********



# Use this command on CloudShell to trip the WAF rule
for i in {1..140}; do curl https://learningawswithlab.net/; done
