# Get User Following with Audius

Retrieves users followed by an Audius user.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id/following`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Get User Following](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
