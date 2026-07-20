# Lookup App by App Store ID with Apple News and Music

Retrieves an app from Apple's catalog by App Store ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup App by App Store ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple App Store track identifier to look up. |
| `entity` | query | `string` | no | Fixed Apple lookup entity. |
