# ARM Template for Asset Monitoring Solution

## Getting Started

The following instructions would help the user to deploy bare minimum Azure resources required to get the solution up and running.

------

### Prerequisites

The following prerequisites are requried to get the Asset Monitoring and Tracking system up and running on a personal account.
* Active Azure subscription.
* Link to the ARM(Azure Resource Manager) template that would be used as a script to install the services.
* Power BI account.
* Access to Power BI templates.

------

### Installing

A step by step series of examples that tell you have to get a development environment running

After achieving the prerequisites, the next step would be the installation of the ARM script. Following are the steps to do the same.
* Login to the Azure portal(https://portal.azure.com) and select the appropriate subscription if it is not selected by default.
* Prepend the acquired ARM template link with "https://portal.azure.com/#create/Microsoft.Template/uri/"  which would look like below else you can also hit the deploy button to deploy the resources.
```
https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2FABC.blob.core.windows.net%2Ftemplates%2FXYZ.json
```
* Once the URL is hit, a form appears which accepts some values before the actual deployment.
* Fill in all the required details using the following guidelines.
    * Preferable use small case characters.
    * **Do Not** use special symbols.
    * Use the **i** image symbol as a guidance for filling in the data.
    * Give special preference to fields marked with **Has to be unique**, as these fields must be unique across the Azure tenant.
    * Bind to the length and other restrictions wherever applicable.
* Once, all the fields have been filled, accept the licensing terms and hit **Purchase**.
* The deployment would take some time;you can have a cup of coffee till then.
* Once you get a notification of successful deployment of resources from Azure, you can proceed with the further steps.
    * Open the web site and follow the pending steps and configurations like configuring a gateway, adding devices, adding the Power BI details etc.
    * Get all the things connected and browse the Power BI reports in web app to see the data coming in.

------

## Setting Up

Before deploying the ARM template, it has to be setup to work for a particular tenant/setup.

There are some placeholders left in the ARM that need to be filled as a part of setting up the script. Majority of the placeholders are URLs of the files uploaded on the blob storage which would be used during deployment of resources like web app, SQL database etc.

A list of the files that need to be uploaded onto the blob storage as follows:
* Web site, Node Server, REST server and Analytics server web deploy packages (.zip file) which could be created using Visual Studio 2015 or later.
* Bacpac file of Azure SQL database (available in **Artifacts** folder)

User needs to copy the link from Azure portal and paste it for respective components mentioned above in the ARM template. 
There are some other placeholders as well, which expects "Storage Account Name", "Storage Account Key", etc. the values for which could also be retrieved from the Azure portal.
Please note that the credentials & details of the storage account to be provided in the ARM template are of the one which contains all the above components in its blob storage. 

------



## Deployment

The ARM template can be deployed using either of the two ways.
* Paste the ARM link in the any of your favourite browsers and hit enter and follow the on screen instructions.
* Hit the **Deploy To Azure** button you have access to and follow the on screen instructions.
