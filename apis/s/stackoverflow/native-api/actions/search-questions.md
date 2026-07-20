# Search Questions with Stackoverflow

Finds questions in Stackoverflow by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://api.stackexchange.com/2.3`
- **Official documentation:** [Search Questions](https://api.stackexchange.com/docs/search)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `site` | query | `string` | yes | Stack Exchange site parameter, for example stackoverflow. |
