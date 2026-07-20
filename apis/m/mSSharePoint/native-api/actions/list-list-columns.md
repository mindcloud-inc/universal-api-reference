# List List Columns with MS SharePoint

Retrieves columns from a SharePoint list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}/columns`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List List Columns](https://learn.microsoft.com/en-us/graph/api/list-list-columns?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
| `listId` | path | `string` | yes | SharePoint list ID. |
