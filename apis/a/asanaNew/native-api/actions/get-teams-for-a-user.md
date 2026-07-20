# Get teams for a user with Asana

Retrieves teams for a user from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_gid/teams`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get teams for a user](https://developers.asana.com/reference/getteamsforuser)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organization` | query | `string` | yes |
| `user_gid` | path | `string` | yes |
