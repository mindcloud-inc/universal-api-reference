# Get memberships from a team with Asana

Retrieves team memberships from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:team_gid/team_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get memberships from a team](https://developers.asana.com/reference/getteammembershipsforteam)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `team_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
