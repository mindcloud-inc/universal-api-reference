# Get Project Status with Zoho Sprints

Retrieves project item statuses from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/itemstatus/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Get Project Status](https://sprints.zoho.com/apidoc.html#Getprojectstatus)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
