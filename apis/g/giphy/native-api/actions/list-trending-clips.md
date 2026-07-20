# List Trending Clips with Giphy

Retrieves trending clips from Giphy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/clips/trending`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [List Trending Clips](https://developers.giphy.com/docs/clips/endpoint/#trending)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `rating` | query | `string` | no |
