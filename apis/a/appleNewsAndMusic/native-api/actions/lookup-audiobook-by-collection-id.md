# Lookup Audiobook by Collection ID with Apple News and Music

Retrieves an audiobook from Apple's catalog by collection ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Audiobook by Collection ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple audiobook collection identifier to look up. |
