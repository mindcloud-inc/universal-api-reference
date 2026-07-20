# Get Item Details with Zoho Sprints

Retrieves item details from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/item/:itemId/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Get Item Details](https://sprints.zoho.com/apidoc.html#Getitemdetails)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
| `itemId` | path | `string` | yes |
