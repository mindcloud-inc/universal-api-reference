# Get User Followers with Audius

Retrieves followers of an Audius user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/followers`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Get User Followers](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
