# Techdoc - DHIaC Template

This is the technical documentation for using the DHIaC Service in Backstage.

## [Parameters](https://github.com/cgallisa/cacorepo01/edit/main/projects/DaC/services/DHIaC/docs/index.md#parameters)
The service will ask the user for the information shown below.

### Service Parameters
Enter the service parameters, which specifies the source location of the table to be replicated:
- Source ... usually an application name or database name where the table to be replicated resides.
- Schema ... Schema name within the *source* stated above.
- Table ... Name of the table to be replicated

### Repository Location
The owner and repository name uniquely identifies the place in GitHub, where the generated code will be stored.
- Owner ... the owner is the first token in GitHub's bread crumb string, top left corner of the screen.
- Repository Name ... we suggest a unique name by concadenating *[source].[schema].[table]* parameters.

### Review
All parameters will be displayed on the screen for review. Press the *CREATE* button if everything looks right.

## [Generated Code](https://github.com/cgallisa/cacorepo01/edit/main/projects/DaC/services/DHIaC/docs/index.md#generated%code)
Upon successful execution of the code, this service will create the following:
- JSON spec ... specification for instantiating the replication job.
- catalog-info.yaml ... specification for registering the new component in Backsatge
- docs ... folder containing documentation for this component.
