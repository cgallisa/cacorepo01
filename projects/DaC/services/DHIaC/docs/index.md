# Techdoc - DHIaC Template

This is the technical documentation for using the DHIaC Service in Backstage.

## Parameters
Backstage `Create` service will ask the user for parameters, as shown below. 

### Service Parameters
Enter the service parameters, which specifies the source location of the table to be replicated:
- `Source` ... usually an application name or database name where the table to be replicated resides.
- `Schema` ... Schema name within the *source* stated above.
- `Table` ... Name of the table to be replicated

### Repository Location
The owner and repository name uniquely identifies the place in GitHub, where the generated code will be stored.
- `Owner` ... the owner is the first token in GitHub's bread crumb string, top left corner of the screen.
- `Repository Name` ... we suggest a unique name by concadenating *[source].[schema].[table]* parameters.

### Review
All parameters will be displayed on the screen for review. Press the `CREATE` button if everything looks right. Backstage will start generating software as described in the next section.

---

## Generated Code
Upon successful execution of the code, this service will create the following:

- `code-DHIaC.json` ... specification for instantiating the replication job.

```json
{
"source": "portico.portown.pp_prac"
"to": "snowflake.portico_core_xxx.portown_pp_prac"
}
```

- `catalog-info.yaml` ... specification for registering the new component in Backsatge, similar to the one below...

```yaml
apiVersion: backstage.io/v1alpha1
kind: Component
metadata:
  name: ${{ values.name | dump }}
  description: This table is ingested from ${{ values.name | dump }} to EDH
  annotations:
    backstage.io/techdocs-ref: dir:.
spec:
  type: service
  owner: user:guest
  lifecycle: POC
```
  
- `docs` ... folder containing documentation for this component, to be rendered in Backstage as `Techdocs`. MD files (markdown) similar to the one below...

```Markdown
# Techdoc - DHIaC Template

This is the technical documentation for using the DHIaC Service in Backstage.

## Parameters
The service will ask the user for the information shown below.
...
...
```
