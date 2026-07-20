# Search with Zendesk

Finds records in Zendesk by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Search](https://developer.zendesk.com/api-reference/ticketing/ticket-management/search/#list-search-results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query string. |
