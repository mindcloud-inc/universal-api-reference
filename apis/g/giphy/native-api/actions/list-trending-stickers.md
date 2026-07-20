# List Trending Stickers with Giphy

Retrieves trending stickers from Giphy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/stickers/trending`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [List Trending Stickers](https://developers.giphy.com/docs/api/endpoint/#trending)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `rating` | query | `string` | no |
