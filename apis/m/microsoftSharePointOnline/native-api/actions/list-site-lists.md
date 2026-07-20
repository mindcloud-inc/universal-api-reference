# List Site Lists with Microsoft SharePoint Online

Retrieves lists from a site in Microsoft SharePoint Online.

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
| `siteId` | path | `string` | yes | Microsoft Graph site ID for the SharePoint site. |
