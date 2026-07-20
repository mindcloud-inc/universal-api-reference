# Lookup App by Bundle ID with Apple News and Music

Retrieves an app from Apple's catalog by bundle ID.

## Endpoint

- **Method:** `GET`
- **Path:** `https://itunes.apple.com/lookup`
- **Base URL:** `https://itunes.apple.com`
- **Official documentation:** [Lookup App by Bundle ID](https://performance-partners.apple.com/search-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bundleId` | query | `string` | yes | Apple app bundle identifier to look up. |
