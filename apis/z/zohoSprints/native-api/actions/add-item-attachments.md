# Add Item Attachments with Zoho Sprints

Adds attachments to an item in Zoho Sprints.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/:teamId/projects/:projectId/sprints/:sprintId/item/:itemId/attachments/`
- **Base URL:** `https://sprintsapi.zoho.com/zsapi`
- **Official documentation:** [Add Item Attachments](https://sprints.zoho.com/apidoc.html#Additemattachments)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `teamId` | path | `string` | yes |
| `projectId` | path | `string` | yes |
| `sprintId` | path | `string` | yes |
| `itemId` | path | `string` | yes |
| `uploadfile` | body | `file` | yes |
