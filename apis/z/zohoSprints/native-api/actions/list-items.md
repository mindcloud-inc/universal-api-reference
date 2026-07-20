# List Items with Zoho Sprints

Retrieves items from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/item/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Items](https://sprints.zoho.com/apidoc.html#Getitems)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
| `searchby` | query | `string` | no |
| `searchvalue` | query | `string` | no |
