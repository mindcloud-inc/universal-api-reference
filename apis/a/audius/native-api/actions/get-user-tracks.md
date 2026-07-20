# Get User Tracks with Audius

Retrieves tracks created by an Audius user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/tracks`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Get User Tracks](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
