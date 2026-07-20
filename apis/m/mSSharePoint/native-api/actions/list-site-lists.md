# List Site Lists with MS SharePoint

Retrieves lists for a SharePoint site.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/lists`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Site Lists](https://learn.microsoft.com/en-us/graph/api/list-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
