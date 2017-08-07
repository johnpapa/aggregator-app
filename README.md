# aggregator app

```bash
az login
```

Create a place to logically store everything (resource group)

```bash
az group create -n PapaStarWarsApiGroup -l eastus
```

Create the storage resource for the Function App

```bash
az storage account create -n papastarwarsapistorage -g PapaStarWarsApiGroup --sku Standard_LRS -l eastus
```

Create the Function App

```bash
az functionapp create -n -g PapaStarWarsApiGroup -s papastarwarsapistorage -c eastus
```
