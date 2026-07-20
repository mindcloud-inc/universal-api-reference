# Lookup AMG Artist Albums with Apple News and Music

Retrieves an artist's albums from Apple's catalog by AMG artist ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup AMG Artist Albums](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `amgArtistId` | query | `string` | yes | AllMusic artist identifier accepted by Apple lookup. |
