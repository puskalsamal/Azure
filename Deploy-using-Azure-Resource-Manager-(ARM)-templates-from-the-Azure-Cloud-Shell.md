You can use Azure Resource Manager (ARM) templates provided by Esri to create the deployments in Microsoft Azure Cloud. You can use the Azure Cloud Shell to launch ARM Templates (as described in this topic).

Prerequisites that are required to be met before launching the stack are listed below.
* Resource Group
* Virtual Network
* Storage Account
* License Files for Server and Portal
* Portal License User Type
* External DNS Name
* SSL Certificate

### Steps to Deploy
1. Launch cloudshell.azure.com in a browser window  (or Azure Portal > Launch cloud shell)
2. Clone this repo using git clone locally and upload the necessary artifacts (DSC.zip, Template File, Template Parameter File, deployArcGISSite.sh) to cloud shell file share.
3. Upload License and Certificate File to cloud shell file share.
4. Make sure the template file and template parameter file of the desired topology, license and certificate files are copied to the same directory as that of the deployArcGISSite.sh script.
5. Edit the ARM Templates parameters file you want to deploy.
6. Navigate to 'clouddrive' folder in cloud shell file share on Azure CloudShell.
7. Use the following command to deploy the ArcGIS Site after replacing the necessary parameters.

```
./deployArcGISSite.sh -f <templateFileName> -p <templateParametersFileName> -g <resourceGroupName> -l <resourceGroupLocation> -s <storageAccountName> -r <storageAccountResourceGroupName>
```

Parameters for `deployArcGISSite.sh` shell script
- f - `templateFileName` is the name of the template file being deployed which is in the same folder as deployArcGISSite.sh shell script (e.g:- basedeployment-single-tier.json).
- p - `templateParametersFileName` is the name of the template parameters file which is in the same folder as deployArcGISSite.sh shell script (e.g:- basedeployment-multi-tier.parameters.json).
- g - `resourceGroupName` is the name of the resource group to deploy into.
- l - `resourceGroupLocation` is the location of the resource group to create in (if not exists).
- s - `storageAccountName` is the name of the storage account used to store deployment artifacts during the deployment.
- r - `storageAccountResourceGroupname` is the name of the resource group for the storageAccountName.