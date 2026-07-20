# Delete Drive Item with Microsoft SharePoint Online

Deletes a drive item from Microsoft SharePoint Online.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/drives/{{driveId}}/items/{{itemId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete Drive Item](https://learn.microsoft.com/en-us/graph/api/driveitem-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID for the SharePoint document library. |
| `itemId` | path | `string` | yes | Microsoft Graph drive item ID. |
