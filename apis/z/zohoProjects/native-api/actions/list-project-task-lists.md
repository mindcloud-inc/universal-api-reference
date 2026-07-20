# List Project Task Lists with Zoho Projects

Retrieves task lists from a Zoho Projects project.

## Endpoint

- **Method:** `GET`
- **Path:** `/portal/[:PORTALID]/projects/[:PROJECTID]/tasklists`
- **Base URL:** `https://projectsapi.zoho.com/api/v3`
- **Official documentation:** [List Project Task Lists](https://projectsapi.zoho.com/api-docs#task-lists_get-all-project-task-lists)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PORTALID` | path | `string` | yes | Zoho Projects portal ID. |
| `PROJECTID` | path | `string` | yes | Zoho Projects project ID. |
