# Search Sites with MS SharePoint

Finds SharePoint sites by search term.

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
| `search` | query | `string` | yes | Search term for SharePoint sites. |
