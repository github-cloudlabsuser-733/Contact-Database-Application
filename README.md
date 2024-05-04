# Web App Deployment to Azure using ARM Templates and GitHub Actions

This repository contains the source code for a web app and the necessary configuration files to deploy the app to Azure using Azure Resource Manager (ARM) templates and GitHub Actions.

## Prerequisites

- An Azure account with an active subscription.
- A GitHub account.

## ARM Template Deployment

The `deploy.json` file in the root of this repository is an ARM template that defines the resources needed for the web app. This includes the web app itself and the hosting plan with a basic/free pricing tier.

To deploy the ARM template:

1. Validate the ARM template using Azure CLI, Azure PowerShell, or the Azure portal.
2. Deploy the ARM template to Azure.

## GitHub Actions Workflow

The `.github/workflows/master_contactdatabaseapp-733.yml` file defines a GitHub Actions workflow that deploys the web app to Azure whenever code is pushed to the repository.

The workflow does the following:

1. Checks out the code.
2. Sets up Azure credentials.
3. Deploys the web app using the `azure/webapps-deploy` GitHub Action.

To set up the workflow:

1. Set the `AZURE_CREDENTIALS` and `AZURE_PUBLISH_PROFILE` secrets in your GitHub repository's settings.
2. Push the workflow file to your GitHub repository.

## Conclusion

With this setup, the web app will automatically be deployed to Azure whenever you push code to your GitHub repository. This allows for a streamlined and efficient deployment process.
