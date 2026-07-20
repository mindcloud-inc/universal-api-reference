# Get Drive Item with Microsoft SharePoint Online

Retrieves a drive item from Microsoft SharePoint Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/{{driveId}}/items/{{itemId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Drive Item](https://learn.microsoft.com/en-us/graph/api/driveitem-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID for the SharePoint document library. |
| `itemId` | path | `string` | yes | Microsoft Graph drive item ID. |
