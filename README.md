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



## Requirements

Component-specific requirements are to be found in the respective READMEs, but there are general requirements too which are listed here.

### A development environment

#### Visual Studio Code

#### Xcode

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

## Contributing

## License
Copyright (c) 2021 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
