# List Folder Project Templates with Taskade

Retrieves project templates from a Taskade folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/project-templates`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List Folder Project Templates](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-project-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
