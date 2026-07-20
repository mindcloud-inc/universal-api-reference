# Create Folder with Microsoft 365

Creates a folder in a Microsoft 365 drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/root:/{{folderPath}}:/children`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Create Folder](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `folderPath` | path | `string` | yes | Path of the parent folder relative to the drive root, such as Documents or Documents/Client Files. |
| `name` | body | `string` | yes | — |
