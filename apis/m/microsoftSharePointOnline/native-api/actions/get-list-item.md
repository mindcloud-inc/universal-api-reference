# Get List Item with Microsoft SharePoint Online

Retrieves a list item from Microsoft SharePoint Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items/{{itemId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get List Item](https://learn.microsoft.com/en-us/graph/api/listitem-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph site ID for the SharePoint site. |
| `listId` | path | `string` | yes | Microsoft Graph list ID or list name for the SharePoint list. |
| `itemId` | path | `string` | yes | Microsoft Graph list item ID. |
