# terraform-vpc-aws
## Usage of this module is as follows
### Create a module.tf file, copy and paste the following code into your module.tf file

```
module "vpc" {
    source                      =   "terraform/vpc/aws"
    region                      =   "${var.region}"
    cidr_block                  =   "${var.cidr_block}"       
    public_cidr1                =   "${var.public_cidr1}"   
    public_cidr2                =   "${var.public_cidr2}"    
    public_cidr3                =   "${var.public_cidr3}"    
    private_cidr1               =   "${var.private_cidr1}"      
    private_cidr2               =   "${var.private_cidr2}"     
    private_cidr3               =   "${var.private_cidr3}"      
    tags                        =   "${var.tags}"
}

```

### Create environments.tfvars file  with the following content. The below is just a sample of your environments.tfvars. You can customize it to meet your requirement.

```
region                      =   "us-east-1"
cidr_block                  =   "10.0.0.0/16"

public_cidr1                =   "10.0.101.0/24"
public_cidr2                =   "10.0.102.0/24"
public_cidr3                =   "10.0.103.0/24"

private_cidr1               =   "10.0.1.0/24"
private_cidr2               =   "10.0.2.0/24"
private_cidr3               =   "10.0.3.0/24"

```


### Run the following commands
``` 
terraform init
```
```
terraform apply -var-file environment.tfvars
