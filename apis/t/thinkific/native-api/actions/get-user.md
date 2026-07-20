# Get User with Thinkific

Retrieves a user record from Thinkific.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Get User](https://developers.thinkific.com/api/api-documentation#/paths/~1users~1{id}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Thinkific user ID or external ID when provider is supplied. |
| `provider` | query | `string` | no | Provider required when using an external user ID. |
