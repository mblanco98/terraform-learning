# Terraform configutation

Is a declaration of resources written in HCL or JSON. It represents the desired state of a set of infrastructure resources.

# Terraform provider

Is a terraform plugin that understands how to work with a specific service provider, such as AWS o Google Cloud Provider.

# Terraform plan

Generates a build execution plan containing all the steps that it will take to converge the current state with the desired state for a set of infrastructure resources.

# Terraform state file

Maintains the current state of a set of resources in a state file.

# Provisioner

Are code or programs that are used to bootstrap resources upon creation. Examples include cloud-init scripts, Cheff, Puppet, etc.

# How does it work

Is a set of instructions that are called along with a terraform provider and terraform itself  handles all the internal states to get to the one that you configured on the HCL config file.


# Build exection plan

You can build an execution plan by running: `terraform plan`.

+ Indicates a resource will be created.
- Indicates a resource will be destroyed.
And -/+ indicates a resources will be destroyed and then re-created.

Execute the plan can be done by running: `terraform apply`.

# Good to know

Terraform files are written in HCL and files end with `.tf`, and terraform CLI loads all files ending in `.tf` by default.

Reserved filenames: `compute.tf`, `provider.tf`, `variables.tf`, `terraform.tfvars`, `compute.auto.tfvars`

Comments are done with: # and /** */

Strings are always in double quotes.

## Provider Syntax

Used to configure a specific cloud service provider

Format: 
````
    provider "aws" {
        access_key = "YOUR_ACCESS_KEY"
        secret_key = "YOUR_SECRET_KEY"
        region = "us-east-1"
    }
````

## Resource Syntax

Used to define infraestructure resources. 

Format:
````
    resource TYPE RESOURCE_NAME {
        attrA = "value1"
        attrB = "value2"
    }
    # TYPE_RESOURCE_NAME can be whatever you want.
````

