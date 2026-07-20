# Create Item with Zoho Sprints

Creates a new item in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/item/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Create Item](https://sprints.zoho.com/apidoc.html#Createitem)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
| `name` | query | `string` | yes |
| `projitemtypeid` | query | `string` | yes |
| `projpriorityid` | query | `string` | yes |
