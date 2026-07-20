# Create Folder with MS SharePoint

Creates a new folder in SharePoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/drives/{{driveId}}/root/children`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Folder](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `name` | body | `string` | yes | Folder name to create. |
