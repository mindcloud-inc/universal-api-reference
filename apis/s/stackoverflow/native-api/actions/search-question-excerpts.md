# Search Question Excerpts with Stackoverflow

Finds question excerpts in Stackoverflow by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/excerpts`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Search Question Excerpts](https://api.stackexchange.com/docs/excerpt-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
| `q` | query | `string` | yes | Full-text search query to excerpt-match. |
