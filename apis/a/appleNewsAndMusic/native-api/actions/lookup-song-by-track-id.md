# Lookup Song by Track ID with Apple News and Music

Retrieves a song from Apple's catalog by track ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Song by Track ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple song track identifier to look up. |
| `entity` | query | `string` | no | Fixed Apple lookup entity. |
