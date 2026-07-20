# Get a user's favorites with Asana

Retrieves a user's favorites from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_gid/favorites`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a user's favorites](https://developers.asana.com/reference/getfavoritesforuser)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `resource_type` | query | `string` | yes |
| `workspace` | query | `string` | yes |
| `opt_fields` | query | `list<string>` | no |
