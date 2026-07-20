# List List Items with MS SharePoint

Retrieves items from a SharePoint list.

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
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
| `listId` | path | `string` | yes | SharePoint list ID. |
