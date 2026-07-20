# List Folder Projects with Taskade

Retrieves projects from a Taskade folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/projects`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List Folder Projects](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
