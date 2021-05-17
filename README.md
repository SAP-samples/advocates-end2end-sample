# Advocates-End2End-Sample
This repository contains the CAP as well as the native iOS app for the End2End example series: **The Advocates Service**

**Contents**

- [Overview](#overview)
- [The Projects](#the-projects)
  - [Advocates Service CAP Service](#advocates-service-cap-service)
  - [Advocates App](#advocates-app)
- [Requirements](#requirements)
  - [A development environment](#a-development-environment)
    - [Visual Studio Code](#vs-code)
    - [Xcode](#xcode)
  - [An SAP BTP trial account](#an-sap-cloud-platform-trial-account)
    - [Trial account](#trial-account)
    - [Cloud Foundry environment](#cloud-foundry-environment)
- [Download and installation](#download-and-installation)
- [Known issues](#known-issues)
- [How to obtain support](#how-to-obtain-support)
- [Contributing](#contributing)
- [License](#license)


## Overview
The Advocates Service is a CAP service being deployed on SAP BTP, Cloud Foundry runtime with a persistence connection to the SAP HANA Cloud. The service itself is holding information about the some Developer Advocates with all the information about the advocates being relevant to its community.

The service is companioned by an Advocates App. This app is written in Swift and uses the SAP BTP SDK for iOS frameworks for data consumption and security. With a mixed UI approach between SwiftUI and UIKit the app code represents a modern approach of native app development.

This repository is structured in its single projects, where each project holds its own purpose. The repository holds all necessary code to run the End2End example of the Advocates Service.

## The Projects

### The Advocates Service
The Advocates Service is a Node.js based SAP Cloud Application Programming Model project which exposes endpoints for OData V2/v4 & REST. The persistence of the Advocates Server is setup in a way that it uses the SAP HANA Cloud on SAP BTP. The project can be build as MTAR and deployed to the SAP BTP, Cloud Foundry runtime.

**Build the project:**
In the root of the project run:
* npm install
* cds build
* cds watch (for local testing)

**Deploy the project:**
Make sure to have installed the MTB command line interface:
* mtb build
* cf deploy <path-to-mtar> (make sure to be logged into CF first)

### The Advocates App
The Advocates App is an Xcode project and needs minimal setup to be build. Please be aware that you need a MacOS system in order to develop for iOS.
1. Change the development team to something valid
2. Make sure the project gets signed for development
3. Create a new Mobile Project on SAP Mobile Services
4. Change the authentication details via the `ConfigurationProvider.plist` file. You can find the needed information in your SAP Mobile Services account.
5. Change the `AppParameters.plist` to match your Application Identifier and has the correct Destination set. You can find the needed information in your SAP Mobile Services account.

**Set-up the SAP Mobile Services app**
In order to use SAP Mobile Services and its features you need to create the Advocates App in your account and make the needed changes to the Xcode project itself to point to the correct cloud configuration.



## Requirements

Component-specific requirements are to be found in the respective READMEs, but there are general requirements too which are listed here.

### A development environment

#### Visual Studio Code / SAP Business Application Studio
The Advocates Service is being implemented with the help of Visual Studio Code, you can also use the SAP Business Application Studio for implementation or replica of the project. 

The benefit of using SAP Business Application Studio in comparisson to Visual Studio Code is that your development environment is fully setup.

* [SAP Business Application Studio](https://developers.sap.com/topics/business-application-studio.html)
* [Visual Studio Code](https://code.visualstudio.com/)

If you need guidance on setting up VS Code for Cloud Application Programming model development you can follow the blog post of [Thomas Jung](https://people.sap.com/thomas.jung):
* https://blogs.sap.com/2020/11/10/vscode-development-for-sap-cloud-application-programming-model-using-remote-wsl/

#### Xcode
The iOS Advocates App is being implemented with Apple Xcode. To develop native iOS apps you need a machine runnning MacOS, for this project the following version is used:

* [Xcode Version 12.5 (12E262) or later](https://developer.apple.com/xcode/)

### An SAP BTP trial account

#### Trial account

You'll need a trial account on SAP BTP, if you haven't got one already. Follow [this tutorial](https://developers.sap.com/tutorials/hcp-create-trial-account.html) for detailed instructions.

#### Cloud Foundry environment

When you set up a trial account, a Cloud Foundry (CF) environment is set up automatically for you, with an organization and single 'dev' space.

> The CF command line interface (CLI) is available as the `cf` command. The version of `cf` required for use in this repository context is version 6. There is a newer version 7 but there is [an issue with version 7 in the use of the `cf env` command](https://github.com/cloudfoundry/cli/issues/2116), which needs to work correctly here. Moreover, it's more likely than not that you have version 6 of `cf` already installed and available.

## Download and installation

To use this repository, **fork it into your own user or org space on GitHub, and then clone that**. You can now follow the component instructions, as well as this main README.

For more information about forking in general, see [Fork a repo](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo) in the GitHub documentation.

Occasionally, we'll add content to this repo.

Throughout the instructions in this repository, the place where you forked this repository too will be referred to in the form "OWNER/REPOSITORY", and you should replace these placeholders with values that are appropriate for you. For example, if you are on GitHub as 'kevinmuessig', and you fork this repository to that space, your values for "OWNER/REPOSITORY" would be "kevinmuessig/Advocates-End2End-Sample".

## Known issues

None at the time of writing.

## How to obtain support

[Create an issue](https://github.com/SAP-samples/<repository-name>/issues) in this repository if you find a bug or have questions about the content.
 
For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## License
Copyright (c) 2021 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
