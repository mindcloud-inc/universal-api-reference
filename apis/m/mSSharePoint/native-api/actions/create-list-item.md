# Create List Item with MS SharePoint

Creates a new item in a SharePoint list.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create List Item](https://learn.microsoft.com/en-us/graph/api/listitem-create?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
| `listId` | path | `string` | yes | SharePoint list ID. |
| `fields` | body | `object` | yes | Object of list item field values to create. |
