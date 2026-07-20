# Advanced Search Questions with Stackoverflow

Finds questions in Stackoverflow with advanced search.

## Endpoint

- **Method:** `GET`
- **Path:** `/search/advanced`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Advanced Search Questions](https://api.stackexchange.com/docs/advanced-search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | API site parameter, for example stackoverflow. |
