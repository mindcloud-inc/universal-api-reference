# List Projects with Zoho Sprints

Retrieves projects from Zoho Sprints.

## Endpoint

- **Method:** `GET`
- **Path:** `/team/:teamId/projects/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [List Projects](https://sprints.zoho.com/apidoc.html#Getprojects)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `index` | query | `number` | yes |
| `range` | query | `number` | yes |
| `projectstatus` | query | `number` | no |
| `viewby` | query | `number` | no |
| `searchvalue` | query | `string` | no |
