# sample-app-for-appservice
My first app service deployment
## Create a reource group
- az group create -- name chris --location eastus
## Create an app service plan  
- az appservice plan create --christoappplan --resource-group chris
## Create a web app  
- az webapp create -- name mrchriswebapp --resource-group chris --plan christoappplan
## Deploy code to the webapp  
az webapp deployment source config --name chrisappdeployment --resource-group --repo-url https://github.com/Olugbamila/sample-app-for-appservice.git --branch master --manual-integration  
