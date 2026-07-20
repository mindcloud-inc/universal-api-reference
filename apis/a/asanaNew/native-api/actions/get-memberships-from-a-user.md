# Get memberships from a user with Asana

Retrieves team memberships for a user from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `users/:user_gid/team_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get memberships from a user](https://developers.asana.com/reference/getteammembershipsforuser)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_gid` | path | `string` | yes | Asana user gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `workspace` | query | `string` | yes | Asana workspace parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
