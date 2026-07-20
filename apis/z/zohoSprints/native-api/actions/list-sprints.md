# List Sprints with Zoho Sprints

Retrieves sprints from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/:projectId/sprints/?action=data&index=1&range=50&type={{sprintTypeArr}}&searchvalue={{searchValue}}`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Sprints](https://sprints.zoho.com/apidoc.html#Getsprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `type` | query | `string` | no |
| `searchvalue` | query | `string` | no |
