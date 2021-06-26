# OSS VNet Peering
VNet peering of OSS Corporation

# Motivation
Connecting Virtual Networks might be messy sometimes if not done right. Creating it, again and again, will be more error-prone. So, we will be utilizing a service from Azure called Azure ARM Templates to deploy our infrastructure in an idempotent way. We will also be using Portal for only some tasks but most of it will be done from the templates.

# Architecture
![architecture](https://user-images.githubusercontent.com/13358738/123504262-d224a000-d677-11eb-94e9-b17376cdead9.png)

# Tools:
1. Azure Account
2. Azure Virtual Machines
3. Azure VNet
4. Azure Templates

# Replication Steps

```bash
git clone git@github.com:codexponent/oss-vnet-peering.git
az group create --name oss-east-rg --location eastus
az group create --name oss-west-rg --location westus
cd east
az deployment group create --resource-group oss-east-rg --template-file template.json 
cd west
az deployment group create --resource-group oss-west-rg --template-file template.json
```

For the rest of the explanation and demonstration I have it on my medium blog.






