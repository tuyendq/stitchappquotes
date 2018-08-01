# stitchappquotes
Microsoft Azure Web App Setup
$resourceGroup="stitchapps"
$appServicePlan="stitchappquotes"
$webApp="azquotes"

az login

az group create --name $stitchapps --location "South Central US"

az appservice plan create --name $appServicePlan --resource-group $resourceGroup --sku FREE

az webapp create --name $webApp --resource-group $resourceGroup --plan $appServicePlan

