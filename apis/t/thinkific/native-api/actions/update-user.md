# Update User with Thinkific

Updates an existing user in Thinkific.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Update User](https://developers.thinkific.com/api/api-documentation#/paths/~1users~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Updated email address. |
| `first_name` | body | `string` | no | Updated first name. |
| `id` | path | `string` | yes | Thinkific user ID or external ID when provider is supplied. |
| `last_name` | body | `string` | no | Updated last name. |
| `provider` | query | `string` | no | Provider required when using an external user ID. |
