# Search Users with Audius

Finds users in Audius by query.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/search`
- **Base URL:** `https://api.audius.co/v1`
- **Official documentation:** [Search Users](https://api.audius.co/v1)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | query | `string` | yes |
| `limit` | query | `number` | no |
| `offset` | query | `number` | no |
