# What I have done so far (azure)

## Create Azure Kubernetes Cluster (AKC)
```
DNS: tstrun-dns-t3x1xv7b.hcp.indonesiacentral.azmk8s.io
```
## Create Azure Container Registry (ACR)
```
registry domain name: tstrunacr.azurecr.io
```

## Using Azure CLI
### Check Azure Version
```
az --version
```

### Azure Login
```
az login --use-device-code
```

### Check Group List
```
az group list --output table
```

### Get Public IP to SSH
```
az vm show --resource-group tstrun_group --name tstrun --show-details --query "publicIps" --output tsv
```

### SSH to azureuser(make sure have key)
```
ssh -i ~/.ssh/tstrunpair.pem azureuser@20.2.138.242
```

### SSH to cloud identity

#### After SSH to azureuser, install azure CLI and login 

```
az ssh vm --resource-group tstrun_group --vm-name tstrun --subscription 2cab04a9-2142-4c11-9d7f-7d5e2cec364f
```

