# Get workspace memberships for a user with Asana

Retrieves a user's workspace memberships from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_gid/workspace_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get workspace memberships for a user](https://developers.asana.com/reference/getworkspacemembershipsforuser)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `user_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
