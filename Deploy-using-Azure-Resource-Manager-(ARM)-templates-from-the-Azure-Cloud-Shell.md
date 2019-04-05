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
* Launch cloudshell.azure.com in a browser window  (or Azure Portal > Launch cloud shell)
* Clone this repo using git clone locally and upload the necessary artifacts (DSC.zip, Template File, Template Parameter File, deployArcGISSite.sh) to cloud shell fileshare.
* Upload License and Cretificate File to cloud shell fileshare.
* Edit the the ARM Templates parameters file you want to deploy.
* Navigate to clouddrive folder in cloud shell fileshare on cloudshell.
* Use the following command to deploy the ArcGIS Site

```
./deployArcGISSite.sh -f <templateFileName> -p <templateParametersFileName> -g <resourceGroupName> -l <resourceGroupLocation> -s <storageAccountName> -r <storageAccountResourceGroupName>
```
