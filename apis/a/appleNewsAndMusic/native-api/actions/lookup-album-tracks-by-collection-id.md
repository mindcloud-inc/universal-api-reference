# Lookup Album Tracks by Collection ID with Apple News and Music

Retrieves an album's tracks from Apple's catalog by collection ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Album Tracks by Collection ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple album collection identifier to expand into track results. |
| `entity` | query | `string` | no | Fixed Apple lookup entity. |
| `limit` | query | `string` | no | Maximum number of track results to return. |
