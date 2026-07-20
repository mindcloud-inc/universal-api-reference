# Search Stickers with Giphy

Finds stickers in Giphy by search phrase.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/stickers/search`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Search Stickers](https://developers.giphy.com/docs/api/endpoint/#search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `lang` | query | `string` | no |
| `q` | query | `string` | yes |
| `rating` | query | `string` | no |
