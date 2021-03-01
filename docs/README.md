## fabAnt

fabAnt is a script wrapper of Salesforce Ant Toolkit used to deploy from org to org, and sooner or later to production.
It's based on Ant that it simplifies and documents. Salesforce release management currently requires a client to temporarly store the metadata to be shipped between orgs. There are no way do do an equivalent operation in the clouds.

Typically you send to the source the name of the components that you need (or a package hosted on the org and that describes them) and then the org send them back to you as they are configured. Of course, classes would contain heavily customized code (that you cannot guess) but most components are also available for description (and migration/deployment). Having said that, Salesforce is renowned for skipping support of some metadata types. You do need to be careful about this area of an org configuration that require manual-pre and manual-post deployment checklists.

fabAnt Will not remove the Salesforce native challenges to release management but will simplify their management by freeing you time to focus on these challenges and automate the easy part of the process.

You must have the following installed on your PC 
### First Installation

### Project Configuration

### User Guide

```batch
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

### (2) Retrieve all supported metadata types

### (3) Download components from manifest

### (4) Download components from the package

### (5) Validate components on the target

### (6) Deploy components on the target

### (7) Delete components on the target

### (8) Quit

