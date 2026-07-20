# List Folder Items with Microsoft SharePoint Online

Retrieves folder items from Microsoft SharePoint Online.

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
| `driveId` | path | `string` | yes | Microsoft Graph drive ID for the SharePoint document library. |
| `folderPath` | path | `string` | yes | Folder path under the drive root, for example Shared Documents/Invoices. |
