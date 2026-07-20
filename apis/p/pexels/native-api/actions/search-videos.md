# Search Videos with Pexels

Finds videos in Pexels by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/videos/search`
- **Base URL:** `https://api.pexels.com`
- **Official documentation:** [Search Videos](https://www.pexels.com/api/documentation/#videos-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Topic to search for, such as Ocean, Tigers, or Group of people working. |
| `orientation` | query | `string` | no | Desired video orientation: landscape, portrait, or square. |
| `size` | query | `string` | no | Minimum video size: large, medium, or small. |
| `locale` | query | `string` | no | Locale for the search, such as en-US, pt-BR, or es-ES. |
