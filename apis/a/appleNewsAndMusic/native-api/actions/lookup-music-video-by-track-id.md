# Lookup Music Video by Track ID with Apple News and Music

Retrieves a music video from Apple's catalog by track ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Music Video by Track ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple music video track identifier to look up. |
| `entity` | query | `string` | no | Fixed Apple lookup entity. |
