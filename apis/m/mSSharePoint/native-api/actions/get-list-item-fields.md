# Get List Item Fields with MS SharePoint

Retrieves field values for a SharePoint list item.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}/fields`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get List Item Fields](https://learn.microsoft.com/en-us/graph/api/listitem-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
| `listId` | path | `string` | yes | SharePoint list ID. |
| `itemId` | path | `string` | yes | SharePoint list item ID. |
