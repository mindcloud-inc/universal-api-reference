# List Workspace Users with Zoho Sprints

Retrieves workspace users from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/users/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Workspace Users](https://sprints.zoho.com/apidoc.html#Getworkspaceusers)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
| `type` | query | `number` | no |
