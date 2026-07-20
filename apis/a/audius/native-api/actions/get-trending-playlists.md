# Get Trending Playlists with Audius

Retrieves trending playlists from Audius.

## Endpoint

- **Method:** `GET`
- **Path:** `/playlists/trending`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Get Trending Playlists](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
| `omit_tracks` | query | `boolean` | no |
