# Search Users with Zendesk

Finds users in Zendesk by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/search.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Search Users](https://developer.zendesk.com/api-reference/ticketing/users/users/#search-users)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query string. Supports Zendesk user search syntax. |
