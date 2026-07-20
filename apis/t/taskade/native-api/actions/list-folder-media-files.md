# List Folder Media Files with Taskade

Retrieves media files from a Taskade folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/:folderId/medias`
- **Base URL:** `https://www.taskade.com/api/v1`
- **Official documentation:** [List Folder Media Files](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-medias)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderId` | path | `string` | yes | Folder ID. |
