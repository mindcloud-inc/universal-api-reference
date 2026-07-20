# Search Drive Items with MS SharePoint

Finds drive items in SharePoint by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/drives/{{driveId}}/root/search(q='{{query}}')`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Search Drive Items](https://learn.microsoft.com/en-us/graph/api/driveitem-search?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Microsoft Graph drive ID. |
| `query` | path | `string` | yes | Search query for drive items. |
