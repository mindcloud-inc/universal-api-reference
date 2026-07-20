# Create Folder with Microsoft SharePoint Online

Creates a folder in Microsoft SharePoint Online.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/drives/{{driveId}}/root/children`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Folder](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID for the SharePoint document library. |
| `name` | body | `string` | yes | Name of the folder to create. |
