# Search Sites with Microsoft SharePoint Online

Finds sites in Microsoft SharePoint Online by keyword.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Search Sites](https://learn.microsoft.com/en-us/graph/api/site-search?view=graph-rest-1.0)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | yes | Search text used by Microsoft Graph to find SharePoint sites. |
