# Search Entities with OpenSanctions

## Endpoint

- **Method:** `GET`
- **Path:** `/search/:dataset`
- **Base URL:** `https://api.opensanctions.org`
- **Official documentation:** [Search Entities](https://api.opensanctions.org/docs#/Matching/search_search__dataset__get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataset` | path | `string` | yes | Data source or collection name to scope the search to. |
| `q` | query | `string` | no | Query text to search for. |
| `schema` | query | `string` | no | Entity schema type to search within. The API default is Thing. |
| `simple` | query | `boolean` | no | Use simple syntax for user-facing query boxes. |
