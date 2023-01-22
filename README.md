
# KPMG Challenge

Technical Challenge

## Challenge 1
A 3-tier environment is a common setup. Use a tool of your choosing/familiarity create these resources. Please remember we will not be judged on the outcome but more focusing on the approach, style and reproducibility

SOLUTION

I have created 3-tier application in Azure using Terraform. Three modules are created for each tier. We can seperate resource based on resource type like network.tf for vnet,subnet, NSG and lb.tf for loadbalancer etc.  but for time being I have kept all in one tf files.

3 Tier Architecture Diagram 


![Logo](https://github.com/saifeeidrish/KPMG_Technical_Challenge/blob/main/3-Tier_Architecture.png)

### Tier-1
Tier-1 (web tier) consist of following Azure resources -
- Subnet for web tier
- Public Load Balancer
- 2 VM's in Availability set for HA
- NSG to allow inbound traffic to VM's

### Tier-2
Tier-2 (app tier) consist of following Azure resources
- Subnet for app tier
- Private Load Balancer
- 2 VM's in Availability set for HA
- NSG to allow inbound traffic to VM's

### Tier-3
Tier-3 (DB tier) consist of following Azure resources -
- Subnet for Database
- NSG to allow traffic from application tier
- Azure SQL Server
- Azure SQL Database
- Private Endpoint to connect DB server with app-tier without going to internet


## Challenge 2
We need to write code that will query the meta data of an instance within AWS and provide a json formatted output. The choice of language and implementation is up to you.

SOLUTION

For my reference I will be using Azure cloud as I am more comfortable in Azure cloud.

I have Written a Shell Script to perform this action .Its an intractive shell scripting and based on your input it will perform the task.

Based on API available I have written the Script . I can perform the same using Poweshell with Invoke-RestMethod .


## Challange 3
We have a nested object, we would like a function that you pass in the object and a key and get back the value. How this is implemented is up to you.

Example Inputs
object = {“a”:{“b”:{“c”:”d”}}}
key = a/b/c
object = {“x”:{“y”:{“z”:”a”}}}
key = x/y/z
value = a


SOLUTION

Written Powershell script to achive this task.
