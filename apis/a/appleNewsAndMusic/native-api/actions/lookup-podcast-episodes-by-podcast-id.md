# Lookup Podcast Episodes by Podcast ID with Apple News and Music

Retrieves podcast episodes from Apple's catalog by podcast ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Podcast Episodes by Podcast ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple podcast identifier to expand into episode results. |
| `entity` | query | `string` | no | Fixed Apple lookup entity. |
| `limit` | query | `string` | no | Maximum number of episode results to return. |
