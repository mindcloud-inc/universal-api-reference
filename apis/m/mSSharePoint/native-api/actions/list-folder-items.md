# List Folder Items with MS SharePoint

Retrieves items from a SharePoint folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/{{driveId}}/root:/{{folderPath}}:/children`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Folder Items](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `folderPath` | path | `string` | yes | Folder path relative to the drive root. |
