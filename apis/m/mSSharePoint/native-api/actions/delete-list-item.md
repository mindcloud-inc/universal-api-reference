# Delete List Item with MS SharePoint

Deletes an item from a SharePoint list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete List Item](https://learn.microsoft.com/en-us/graph/api/listitem-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
| `listId` | path | `string` | yes | SharePoint list ID. |
| `itemId` | path | `string` | yes | SharePoint list item ID. |
