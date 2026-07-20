# Lookup by AMG Artist ID with Apple News and Music

Retrieves a catalog item from Apple's catalog by AMG artist ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup by AMG Artist ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amgArtistId` | query | `string` | yes | AllMusic artist identifier accepted by Apple lookup. |
