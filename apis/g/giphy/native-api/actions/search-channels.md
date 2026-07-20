# Search Channels with Giphy

Finds channels in Giphy by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/channels/search`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Search Channels](https://developers.giphy.com/docs/api/endpoint/#channel-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
