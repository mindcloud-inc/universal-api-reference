# Search Entities with Optimizely

Finds entities in Optimizely by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.optimizely.com/v2`
- **Official documentation:** [Search Entities](https://docs.developers.optimizely.com/web-experimentation/reference/get_search_results)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | The search text. |
