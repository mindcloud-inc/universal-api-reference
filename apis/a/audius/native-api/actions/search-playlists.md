# Search Playlists with Audius

Finds playlists in Audius by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/playlists/search`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Search Playlists](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
