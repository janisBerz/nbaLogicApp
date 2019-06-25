# Azure Logic App
Using this ARM template you'll be able to provision a Azure Logic App that pulls list of NBA players from the **standard** league. The logic app is configured to run once a week.

## Usage
Assuming you have a resource group with name **nbaLogicApp** that contains a configured Azure Blob Storage API Connection **azureblob** and Gmail API connection **gmail** use the following PowerShell Command to deploy the ARM template.

```powershell
New-AzureRmResourceGroupDeployment -ResourceGroupName nbaLogicApp -TemplateFile .\nbaLogicApp\LogicApp.json -TemplateParameterFile .\nbaLogicApp\LogicApp.parameters.json
```
Please keep in mind that the API Connections have to be in the same Resource Group where you are deploying the Logic App.
