# Delete List Item with Microsoft SharePoint Online

Deletes a list item from Microsoft SharePoint Online.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Delete List Item](https://learn.microsoft.com/en-us/graph/api/listitem-delete?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph site ID for the SharePoint site. |
| `listId` | path | `string` | yes | Microsoft Graph list ID or list name for the SharePoint list. |
| `itemId` | path | `string` | yes | Microsoft Graph list item ID. |
