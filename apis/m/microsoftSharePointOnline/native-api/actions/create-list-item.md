# Create List Item with Microsoft SharePoint Online

Creates a list item in Microsoft SharePoint Online.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create List Item](https://learn.microsoft.com/en-us/graph/api/listitem-create?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph site ID for the SharePoint site. |
| `listId` | path | `string` | yes | Microsoft Graph list ID or list name for the SharePoint list. |
| `fields` | body | `object` | yes | Object containing SharePoint list column values for the new item. |
