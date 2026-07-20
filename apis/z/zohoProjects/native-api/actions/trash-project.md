# Trash Project with Zoho Projects

Trashes an existing project in Zoho Projects.

## Endpoint

- **Method:** `POST`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/trash`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [Trash Project](https://projectsapi.zoho.com/api-docs#projects_trash-a-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Portal identifier from Zoho Projects. |
| `PROJECTID` | path | `string` | yes | Project identifier from Zoho Projects. |
