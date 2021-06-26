# oss-vnet-peering
VNet peering of OSS Corporation


az group create --name oss-east-rg --location eastus
az group create --name oss-west-rg --location westus

az deployment group create --resource-group oss-east-rg --template-file template.json 
az deployment group create --resource-group oss-west-rg --template-file template.json

