# List Project Priorities with Zoho Sprints

Retrieves project priorities from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/priority/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Project Priorities](https://sprints.zoho.com/apidoc.html#Getprojectpriorities)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
