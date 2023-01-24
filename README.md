# azure-webapp-static-hugo

A demo how to create a static website using hugo and publish it as an Azure App Service

## Building

```sh
hugo -d ../dist -s ./src
```

## Deployment: Option 1

### Provisioning

```sh
az login
az account set --subscription "Visual Studio Professional Subscription"
az group create --resource-group Hugo-WUS --location westus
```

### Deployment

```sh
az webapp up --html --resource-group "Hugo-WUS" --location "westus" --name wshugo129382
```

### Testing

```sh
curl https://wshugo129382.azurewebsites.net
```
