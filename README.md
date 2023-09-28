# ZeroWaste App

## Summary

Zero waste app leverages AI to help avoid wating food and managing the food inventory in an efficient way.

It integrates AI builder object recognition to scan a fridge or a shelf, and tell exactly what is missing from the pre-defined shopping list.

So, there are 4 parts:

 - 'Camera', where user can leverage AI builder to scan his fridge and calculate the shopping list
 - 'My List' where the user defines what he needs to buy
 - 'Shopping list' where the user will find the calculated shopping list, based on the scan made by AI builder
 - 'Recipes' where user can leverage chat GPT to get recipies with the already existent items, and then save the ones that he finds useful
 - 'Settings' where the user can define his profile and inform the app about some food restrictions, etc.


Main components:

 - One zip folder that contains 2 Custom connectors that are linked together to communicate with Walmart API.
 - Power Automate flow to leverage the developed webservice and Walmart API through custom connectors
 - Canvas app
 - AI model already trained

---
page_type: Managed App solution
languages:
- powerapps-comma
products:
- powerapps
- canvas
name: ZeroWaste App
description: Managed production solution of the mobile version of ZeroWaste PowerApp
ms.date: 9/28/2023
authors: edgarsimoes, gabrielouteiro, alexandretoupa
level: intermediate
ms.prod: power-apps
---


## Applies to

* [Microsoft Power Apps](https://docs.microsoft.com/powerapps/)

## Compatibility

![Power Apps Source File Pack and Unpack Utility 0.20](https://img.shields.io/badge/Packing%20Tool-0.20-green.svg)
![Premium License](https://img.shields.io/badge/Premium%20License-Not%20Required-green.svg "Premium Power Apps license not required")
![Experimental Features](https://img.shields.io/badge/Experimental%20Features-No-green.svg "Does not rely on experimental features")
![On-Premises Connectors](https://img.shields.io/badge/On--Premises%20Connectors-No-green.svg "Does not use on-premise connectors")
![Custom Connectors](https://img.shields.io/badge/Custom%20Connectors-Not%20Required-green.svg "Does not use custom connectors")

## Authors

Solution|Author(s)
--------|---------
ZeroWaste Solution | [Edgar Simões](https://github.com/edgarsimoes), [Gabriel Outeiro](https://github.com/gabrielouteiro), [Alexandre Santos](https://github.com/alexandretoupa)

## Version history

Version|Date|Comments
-------|----|--------
1.0|September 28, 2023|Initial release


## Features

This sample illustrates the following concepts:

* PowerApps mobile canvas app
* Power Automate Cloud Flow
* Walmart Custom Connector
* Dataverse table
* AI Builder Object Detector
* AI Builder Create Text with GPT (Preview - Need US environment and still may not be available)

## Prerequisites

### Using the Solution

* Need to create two valid connections for the custom connector.
* First leverage Walmart API: https://www.walmart.io/docs/affiliate/
* Next, create a web app on Java according to the API script instructions: https://www.walmart.io/docs/affiliate/onboarding-guide. This Generated signature script will supply a signature key that is required to use on one of the API headers. Note: We suggest you to host the Java project on Azure to later use as input on the Walmart custom connector that contains the actions to Search product items and also to post on a Walmart cart all the selected porducts.
* Import the custom connector zip folder to leverage first the GetSignature custom connector that should follow the steps we mentioned before, and then use in a Power Automate Cloud Flow on a step that is previous to use the Walmart I/O Custom connector due to the fact that you will need the GetSignature output.
  
```

## Data Sources
 
ProductsDemo Dataverse table that is the AI Builder Object Detection Dataset.
All the rest in runned on local PowerApp collections and stored in cache.

## Minimal Path to Awesome

* [Download](./solution/ZeroWaste.msapp) the `.msapp` from the `solution` folder
* Use the `.msapp` file using **File** > **Open** > **Browse** within Power Apps Studio.
* Save and Publish

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

## Support

While we don't support samples, if you encounter any issues while using this sample, you can [create a new issue]([https://github.com/devnovasbe/PP_AI_Global_Hackathon/issues]).
