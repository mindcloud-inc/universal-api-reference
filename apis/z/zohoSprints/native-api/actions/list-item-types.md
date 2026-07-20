# List Item Types with Zoho Sprints

Retrieves item types from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/itemtype/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Item Types](https://sprints.zoho.com/apidoc.html#Getitemtypes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
