# List Trending GIFs with Giphy

Retrieves trending GIFs from Giphy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/gifs/trending`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [List Trending GIFs](https://developers.giphy.com/docs/api/endpoint/#trending)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `rating` | query | `string` | no |
