# Lookup Book by ISBN with Apple News and Music

Retrieves a book from Apple's catalog by ISBN.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Book by ISBN](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isbn` | query | `string` | yes | ISBN for a book in Apple's catalog. |
