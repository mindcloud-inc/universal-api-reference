# Get a team membership with Asana

Retrieves a team membership from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `team_memberships/:team_membership_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a team membership](https://developers.asana.com/reference/getteammembership)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `team_membership_gid` | path | `string` | yes |
| `opt_pretty` | query | `boolean` | no |
| `opt_fields` | query | `list<string>` | no |
