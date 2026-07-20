# Search Trunks with PBX Yeastar

Finds trunks in PBX Yeastar by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/trunk/search`
- **Base URL:** `{baseUrl}/openapi/v1.0`
- **Official documentation:** [Search Trunks](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specfic-trunks.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_value` | query | `string` | no | Search keyword for filtering trunks. |
