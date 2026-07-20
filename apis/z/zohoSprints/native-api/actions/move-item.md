# Move Item with Zoho Sprints

Moves items to another sprint in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/bulkupdate/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Move Item](https://sprints.zoho.com/apidoc.html#Moveitem)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
| `itemidarr` | query | `string` | yes |
| `tosprintid` | query | `string` | yes |
| `toprojectid` | query | `string` | yes |
