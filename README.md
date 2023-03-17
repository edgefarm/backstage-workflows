# Backstage workflows

This repo contains all workflows, which we as EdgeFarm operator offer to our customers in Edgefarm.

# Installation

Add the following to your backstage configuration file `app_config.yaml`:

```yml
catalog:
  locations:
    - type: url
      target: https://github.com/edgefarm/backstage-workflows/blob/main/all.yaml
      rules:
        - allow: [Template]

```

For the local environment, the file itself can also be loaded instead of the URL

```yml
    - type: file
      target: ../../../backstage-workflows/all.yaml
      rules:
        - allow: [Template]
```

Backstage will read and process the locations at startup. The workflows are then available as templates at http://localhost:3000/create.