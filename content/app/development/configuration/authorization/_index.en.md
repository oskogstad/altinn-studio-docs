---
title: Authorization
linktitle: Authorization
description: How to define authorization rules (access management) for an app.
weight: 100
---

Authorization rules for an application is defined in a XACML policy file which is placed in the app repository.
The XACML Policy contains one or more rules which define who can perform different actions on different resources.

Description of the XACML structure and definition of rules can be found [here](/technology/architecture/components/application/solution/altinn-studio/designer/pap/xacmlpolicy/)

The XACML file can be edited in a text editor of your choice.

## Rules from the application template
When an app is created in Altinn Studio it is based an the current asp.net template, and will include an autogenerated XACML policy file.
The rules that are defined in this file is described below.  

The aforementioned rules can be changed in *policy.xml* which lies in `App/config/authorization` in the application repository.
Details about configuring the policy file can be found [here](/technology/architecture/components/application/solution/altinn-studio/designer/pap/xacmlpolicy/
You can also find a good amount of example rules [here](rules).

{{%notice warning%}}
Please note that changes to the policy file is at your own risk,
and that it is recommended to always delegate read permissions to entities with writing permissions.
{{% /notice%}}

### Permissions for roles
The rules that give the CEO (DAGL) or accountant assistant (REGNA) permissions to instantiate, write 
read and delete instances of the application are defined in the policy file.

A complete list of role types can be found [here](https://www.altinn.no/api/metadata/roledefinitions).

### Permissions for the application owner
The application owner (organization) has rights to instantiate, write and read instances of the application.
They also have permissions to mark instances as completed. 

### Required authentication level
Reqired authentication level is set to 2 by default. This is done as an obligation in the XACML Policy file. 

If the required authentication level is set to 4 you have to define that the service owner can interact with it through level 3 authentification for Maskinporten.
This is because Maskinporten is defined as level 3. See the rule library for examples. Notice: the app requires nuget version`3.1.5` or higher.

{{% children description="true" %}}