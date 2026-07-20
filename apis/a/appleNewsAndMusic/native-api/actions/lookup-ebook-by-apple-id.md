# Lookup Ebook by Apple ID with Apple News and Music

Retrieves an ebook from Apple's catalog by Apple ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Ebook by Apple ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple ebook identifier to look up. |
| `entity` | query | `string` | no | Fixed Apple lookup entity. |
