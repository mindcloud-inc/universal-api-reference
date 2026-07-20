# Get User Playlists with Audius

Retrieves playlists created by an Audius user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/playlists`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Get User Playlists](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
