---
title: SCP Primary Tag Tutorial One
description: Set up trust between SAP Cloud Platform Identity Authentication Service
primary_tag: products>73555000100700000172
tags: [  tutorial>beginner, topic>abap-development, topic>abap-extensibility ]
time: 25
author_name: Ulrike Liebherr
author_profile: https://github.com/Liebherr
---

## Prerequisites
**Authorizations**: Your user needs
- Administrator access to your **SAP Cloud Platform** subaccount
- Administrator access to your **SAP Cloud Platform Identity Authentication tenant**

## Details
### Glossary
**Identity**: individual people, but also computers, services, computational entities like processes and threads, or any group of such things
**SAP Cloud Platform Identity Authentication Service**: SAP's solution to enable identity authentication, abbreviated as **IAS**

### You will learn
- How to set up SAP Cloud Platform Subaccount for secure communication (with Security Assertion Markup Language = SAML 2.0)
- How to set up SAP Cloud Platform Subaccount on SAP Cloud Platform Identity Authentication Service for secure communication
- How to get necessary information from your SAP Cloud Platform Subaccount and your SAP Cloud Platform Identity Authentication tenant to set up the mutual trust between them

### Additional Information
- **Documentation:** [SAP Cloud Platform Identity Authentication Service](https://help.sap.com/viewer/6d6d63354d1242d185ab4830fc04feb1/Cloud/en-US/d17a116432d24470930ebea41977a888.html)
- **SAP S/4HANA Cloud Release** (tutorial's last update): 1911
---

[ACCORDION-BEGIN [Step 1: ](Enter trust management of subaccount)]
Enter the SAP Cloud Platform subaccount as an administrator and expand the **Security** area to open Trust Management by clicking the **Trust** section.

![Enter SAP Cloud Platform Subaccount]

[DONE]
[ACCORDION-END]

[ACCORDION-BEGIN [Step 2: ](Set subaccount as service provider)]
To enable secure (Security Assertion Markup Language = SAML 2.0) communication the SAP Cloud Platform Subaccount has to be set up as Service Provider.

Being in the trust management, click **Edit** to change the default Local Service Provider.

![Edit local service provider]
Change and add following information to your local provider:

| ------------------------------------------- | ------------------------------------------- |
|           **Configuration Type**            |                    `Custom`                   |
|           **Local Provider Name**           | `<platform region s URL>/<subaccount name>` (set automatically) |
|          **Principal Propagation**          |                 `Enabled`                 |
|          **Force Authentication**           |               `Disabled`            |

Click **Generate Key Pair**

![Generate Key Pair for and save Local Service Provider]

**Save** your changes.

[DONE]
[ACCORDION-END]

