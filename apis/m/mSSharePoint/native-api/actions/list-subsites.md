# List Subsites with MS SharePoint

Retrieves subsites for a SharePoint site.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/sites`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Subsites](https://learn.microsoft.com/en-us/graph/api/site-list-subsites?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
