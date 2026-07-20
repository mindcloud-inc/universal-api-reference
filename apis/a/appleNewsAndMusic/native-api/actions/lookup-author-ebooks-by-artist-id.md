# Lookup Author Ebooks by Artist ID with Apple News and Music

Retrieves an author's ebooks from Apple's catalog by artist ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Author Ebooks by Artist ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Apple iTunes artist identifier to expand into ebook results. |
