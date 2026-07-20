# Lookup Album by UPC with Apple News and Music

Retrieves an album from Apple's catalog by UPC.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup Album by UPC](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `upc` | query | `string` | yes | Universal Product Code for an album in Apple's catalog. |
