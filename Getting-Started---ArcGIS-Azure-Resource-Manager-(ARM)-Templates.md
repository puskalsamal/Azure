You can use Azure Resource Manager (ARM) Templates provided by ESRI to deploy following architectures
- A single machine ArcGIS Enterprise deployment
- A two machine ArcGIS Enterprise deployment
- A highly available ArcGIS Enterprise site
- A single machine ArcGIS Server site
- A highly available ArcGIS Server site
- A single machine ArcGIS GeoAnalytics Server site
- A highly available ArcGIS GeoAnalytics Server site
- A single machine ArcGIS GeoEvent Server site
- A highly available ArcGIS GeoEvent Server site
- A single machine ArcGIS Image/Raster Server site
- A highly available ArcGIS Image/Raster Server site
- A single machine ArcGIS Notebook Server site

You can also copy and modify these templates to fit your specific needs, or create your own templates to implement your own deployment patterns.

You can work with ARM templates directly using Command Line or using Azure Cloud Shell.

Azure ARM Templates is a service that helps you define architectures on Microsoft Azure. It is an example of infrastructure as code, meaning you write code that can deploy a particular hardware infrastructure in a cloud environment. In the case of ARM Templates, you use a JavaScript object notation (JSON) template to define a stack of resources that work together in a predetermined way.

Using ARM templates also makes launching and maintaining a deployment easier than doing it manually and allows you to set up identical architectures in different Azure accounts or regions.


## ARM Templates

Esri provides ARM templates through GitHub, from which you can download them. Templates are specific to an ArcGIS release.


## Deploy ArcGIS Enterprise using ARM Template
ARM templates are available to deploy ArcGIS Enterprise on Azure. ArcGIS Enterprise deployments include the following ArcGIS components:

- Portal for ArcGIS
- ArcGIS Server
- ArcGIS Data Store

In addition to the above ArcGIS Enterprise components, a load balancer and webproxy might be deployed depending on the type of deployment.

You need the following before you can run the Azure Resource Manager (ARM) templates to deploy ArcGIS Enterprise:

- Licesnse File for server and portal
- A valid domain name for your site. 
- A TLS (SSL) certificate for your domain, obtained from a certifying authority.




