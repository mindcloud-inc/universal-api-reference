# Search Extensions with PBX Yeastar

Finds extensions in PBX Yeastar by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/extension/search`
- **Base URL:** `{baseUrl}/openapi/v1.0`
- **Official documentation:** [Search Extensions](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-extensions.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_value` | query | `string` | no | Search keyword for filtering extensions. |
