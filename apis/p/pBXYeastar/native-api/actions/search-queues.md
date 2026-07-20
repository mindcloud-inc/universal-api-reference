# Search Queues with PBX Yeastar

Finds queues in PBX Yeastar by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/queue/search`
- **Base URL:** `{baseUrl}/openapi/v1.0`
- **Official documentation:** [Search Queues](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-queues.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_value` | query | `string` | no | Search keyword for filtering queues. |
