# List List Items with Microsoft SharePoint Online

Retrieves list items from Microsoft SharePoint Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/items`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List List Items](https://learn.microsoft.com/en-us/graph/api/listitem-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph site ID for the SharePoint site. |
| `listId` | path | `string` | yes | Microsoft Graph list ID or list name for the SharePoint list. |
