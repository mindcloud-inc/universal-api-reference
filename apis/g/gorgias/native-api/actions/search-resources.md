# Search Resources with Gorgias

Finds resources in Gorgias by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://{subdomain}.gorgias.com/api`
- **Official documentation:** [Search Resources](https://developers.gorgias.com/reference/search-1)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Search query text. |
