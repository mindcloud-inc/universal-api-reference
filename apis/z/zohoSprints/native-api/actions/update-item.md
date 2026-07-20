# Update Item with Zoho Sprints

Updates an existing item in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/item/:itemId/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Update Item](https://sprints.zoho.com/apidoc.html#Updateitem)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
| `itemId` | path | `string` | yes |
| `name` | body | `string` | no |
| `projitemtypeid` | body | `string` | no |
| `projpriorityid` | body | `string` | no |
| `statusid` | body | `string` | no |
| `epicid` | body | `string` | no |
| `description` | body | `string` | no |
| `point` | body | `number` | no |
| `startdate` | body | `date` | no |
| `enddate` | body | `date` | no |
