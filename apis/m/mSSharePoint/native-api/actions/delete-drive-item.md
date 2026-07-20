# Delete Drive Item with MS SharePoint

Deletes a SharePoint drive item.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/drives/{{driveId}}/items/{{itemId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete Drive Item](https://learn.microsoft.com/en-us/graph/api/driveitem-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `itemId` | path | `string` | yes | Drive item ID. |
