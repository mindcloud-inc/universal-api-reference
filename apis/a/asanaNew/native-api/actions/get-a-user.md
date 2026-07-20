# Get a user with Asana

Retrieves a user from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a user](https://developers.asana.com/reference/getuser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opt_fields[]` | query | `array<string>` | no | — |
| `user_gid` | path | `string` | yes | Path parameter: user_gid |
