# Search Clips with Giphy

Finds clips in Giphy by search phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/clips/search`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Search Clips](https://developers.giphy.com/docs/clips/endpoint/#search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
| `rating` | query | `string` | no |
