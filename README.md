# terraform-vpc-aws
## Usage of this module is as follows
### Create a module.tf file, copy and paste the following code into your module.tf file

```
module "vpc" {
    source                      =   "ceagone/vpc/aws"
    version                     =   "1.0.0"
    region                      =   "us-east-1"
    cidr_block                  =   "10.0.0.0/16"
    public_cidr1                =   "10.0.101.0/24"
    public_cidr2                =   "10.0.102.0/24"
    public_cidr3                =   "10.0.103.0/24"
    private_cidr1               =   "10.0.1.0/24"
    private_cidr2               =   "10.0.2.0/24"
    private_cidr3               =   "10.0.3.0/24"
    
    tags    =   {
    Name                    =   "Bola-VPC"
    Environment             =   "Dev"
    Team                    =   "DevOps"
    Department              =   "IT"
   }
}

```

### The above is just a sample. You can customize your code how you want it.

### Run the following commands
``` 
terraform init
```
```
terraform apply
```
