# DaC
Data as Code - Template of Templates

This service creates other DaC templates (i.e. for DHIaC, DMaC, DPaC, etc.), to be registered in Backstage. It creates skeleton files, meaning not all template details such as parameters and steps are created. See TechDocs for full details.

## Content

- `docs` ... folder containing document-as-code files, for this template.

- `README.md` ... file containing a description of this folder. This text is displayed by GitHub UI as you navigate to this location.
  
- `catalog-info.yaml` ... contains specs for this template to be registered, within Backstage Catalog.
  
- `mkdocs.yml` ... contains specs for the rendering of this teamplate's documentation, within Backsatge Docs.

- `template.yaml` ... contains specs for the template to behave, within Backstage Create. When invoked by a user, it includes rendering of parms, execution of steps, etc.
