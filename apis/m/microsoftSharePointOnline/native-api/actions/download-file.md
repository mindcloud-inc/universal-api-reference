# Download File with Microsoft SharePoint Online

Downloads a file from Microsoft SharePoint Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/{{driveId}}/items/{{itemId}}/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Download File](https://learn.microsoft.com/en-us/graph/api/driveitem-get-content?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID for the SharePoint document library. |
| `itemId` | path | `string` | yes | Microsoft Graph drive item ID for the file. |
