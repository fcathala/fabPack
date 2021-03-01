# fabAnt

fabAnt is a script wrapper of Salesforce Ant Toolkit used to deploy from org to org, and sooner or later to production.
It's based on Ant that it simplifies and documents. Salesforce release management currently requires a client to temporarly store the metadata to be shipped between orgs. There are no way do do an equivalent operation in the clouds.

Typically you send to the source the name of the components that you need (or a package hosted on the org and that describes them) and then the org send them back to you as they are configured. Of course, classes would contain heavily customized code (that you cannot guess) but [most components](https://developer.salesforce.com/docs/metadata-coverage) are also available for description (and migration/deployment). Having said that, Salesforce is renowned [for skipping support of some metadata types](https://help.salesforce.com/articleView?id=sf.changesets_about_components.htm&type=5) (although, to be accurate, what's available in change Set and what's available in the metadata API is not the same thing). You do need to be careful about this area of an org configuration that require manual-pre and manual-post deployment checklists.

fabAnt will not remove the Salesforce native challenges to release management but will simplify their management by freeing you time to focus on these challenges and automate the easy part of the process.

## First Installation

Although you may argue that this is a painful step, requiring computer troubleshooting at times, it's also a one-off thing to do to accomodate your computer to this way of working with Salesforce orgs.

To run fabAnt you must have the following installed on your computer:

* [Java](https://www.azul.com/downloads/zulu-community/?package=jdk) ~ Attention [Oracle](https://www.oracle.com/uk/downloads/licenses/javase-license1.html) JDK is not Open Source any more. There are some ways around it but the best is to change sowftare altogether and go with [Azul](https://www.azul.com/products/zulu-enterprise/jdk-comparison-matrix/) for instance which is Salesforce's recommended Java Client for the Data Loader as well...
* [Ant](https://ant.apache.org/manual/install.html)
* [Salesforce toolkit for Ant](https://developer.salesforce.com/docs/atlas.en-us.daas.meta/daas/forcemigrationtool_install.htm)
* [fabAnt](https://github.com/fcathala/fabAnt/archive/master.zip) ~ Download both the PC and Mac versions

## Project Configuration

In the first versions (v1.x) I was trying to limit the number of installation to a single Salesforce Toolkit per computer (as there is a single install of Java or Ant). In the following versions, I have changed this architecture to come bak to something simpler to use. As a result there will be quite a few duplicates but Salesforce manages old versions quite well, so no need to be stressed about that. An install is now **Project Centric** and within a **Project** each folder must represent a pair of source and destination orgs. Example for a 3 orgs structure, you would have to configure your folders this way:

```
C:\USERS\<YOUR_NAME>\<PROJECT_NAME>\DEV-QA
│   │   fabAnt.cmd
│   ├───jar
│   │       ant-salesforce.jar
│   └───lib
│           deployCode.cmd
│           deployCodeCheckOnly.cmd
│           describeMetadata.cmd
│           fabAnt.xml
│           org.down.properties
│           org.up.properties
│           retrieveCode.cmd
│           retrievePkg.cmd
│           testInstallation.cmd
│           undeployCode.cmd
│
└───QA-SIT
│   │   fabAnt.cmd
│   ├───jar
│   │       ant-salesforce.jar
│   └───lib
│           deployCode.cmd
│           deployCodeCheckOnly.cmd
│           describeMetadata.cmd
│           fabAnt.xml
│           org.down.properties
│           org.up.properties
│           retrieveCode.cmd
│           retrievePkg.cmd
│           testInstallation.cmd
│           undeployCode.cmd
│
└───SIT-PROD
    ant-salesforce.jar
    ├───jar
    │       ant-salesforce.jar
    └───lib
            deployCode.cmd
            deployCodeCheckOnly.cmd
            describeMetadata.cmd
            fabAnt.xml
            org.down.properties
            org.up.properties
            retrieveCode.cmd
            retrievePkg.cmd
            testInstallation.cmd
            undeployCode.cmd
```

1. The folders "**DEV-QA**", "**QA-SIT**" and "**SIT-PROD**" should host 3 migrations from "**DEV**" to "**QA**", "**SIT**" and "**PROD**". You must configure the files "org.down.properties" and "org.up.properties" accordingly (down = source, up = target). There is some room for flexibility here depenmding on how comfortable are you doing it. These folders contain a download from this Git repo which supports both PC and Mac, so you can simplify the folder structure as you prefer (I always get rid of the folder I am not using and move the content of the other to my orgs-duo root).
2. In the "jar" folder you must copy the latest toolkit obtained from [Salesforce](https://developer.salesforce.com/docs/atlas.en-us.daas.meta/daas/forcemigrationtool_install.htm) (ant-salesforce.jar).

## User Guide

```
----------------------------------------------------------
 fabPack - Packaging Utility for Salesforce Professionals
----------------------------------------------------------

 (1) Check installation
 (2) Retrieve all supported metadata types
 (3) Download components from manifest
 (4) Download components from the package
 (5) Validate components on the target
 (6) Deploy components on the target
 (7) Delete components on the target
 (8) Quit

----------------------------------------------------------

Please, type the selection number from 1 to 8.
```

### (1) Check installation

### (2) Retrieve metadata types

### (3) Download from manifest

### (4) Download from package

### (5) Validate on the target

### (6) Deploy on the target

### (7) Delete on the target

### (8) Quit

