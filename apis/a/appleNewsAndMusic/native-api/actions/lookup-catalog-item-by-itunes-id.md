# Lookup Catalog Item by iTunes ID with Apple News and Music

Retrieves a catalog item from Apple's catalog by iTunes ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Catalog Item by iTunes ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple iTunes identifier to look up, such as an artist, album, or track ID. |
