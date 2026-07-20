# List Site Drives with MS SharePoint

Retrieves drives for a SharePoint site.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/drives`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [List Site Drives](https://learn.microsoft.com/en-us/graph/api/drive-list?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
