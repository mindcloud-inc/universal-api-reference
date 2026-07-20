# List Folder Items with Microsoft 365

Retrieves items in a folder from Microsoft 365.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/me/drive/root:/{{folderPath}}:/children`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [List Folder Items](https://learn.microsoft.com/en-us/graph/api/driveitem-list-children?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderPath` | path | `string` | yes | Path of the folder to list relative to the drive root, such as Documents or Documents/Client Files. |
