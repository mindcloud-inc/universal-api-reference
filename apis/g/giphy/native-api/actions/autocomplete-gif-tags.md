# Autocomplete GIF Tags with Giphy

Finds autocomplete tag terms for GIFs in Giphy.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/gifs/search/tags`
- **Base URL:** `https://api.giphy.com/`
- **Official documentation:** [Autocomplete GIF Tags](https://developers.giphy.com/docs/api/endpoint/#autocomplete)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `q` | query | `string` | yes |
