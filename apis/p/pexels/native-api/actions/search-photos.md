# Search Photos with Pexels

Finds photos in Pexels by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/search`
- **Base URL:** `https://api.pexels.com`
- **Official documentation:** [Search Photos](https://www.pexels.com/api/documentation/#photos-search)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Topic to search for, such as Ocean, Tigers, or Group of people working. |
| `orientation` | query | `string` | no | Desired photo orientation: landscape, portrait, or square. |
| `size` | query | `string` | no | Minimum photo size: large, medium, or small. |
| `color` | query | `string` | no | Desired photo color name or hex color code supported by Pexels. |
| `locale` | query | `string` | no | Locale for the search, such as en-US, pt-BR, or es-ES. |
