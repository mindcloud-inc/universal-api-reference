# Update Subfolder with Wistia

Updates an existing subfolder in Wistia.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/projects/:projectId/subfolders/:subfolderId`
- **Base URL:** `https://api.wistia.com`
- **Official documentation:** [Update Subfolder](https://docs.wistia.com/reference/put_projects-projectid-subfolders-subfolderid)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `string` | yes |
| `subfolderId` | path | `string` | yes |
| `name` | body | `string` | no |
