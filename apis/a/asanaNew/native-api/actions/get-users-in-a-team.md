# Get users in a team with Asana

Retrieves users in an Asana team.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:team_gid/users`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get users in a team](https://developers.asana.com/reference/getusersforteam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_gid` | path | `string` | yes | Asana team gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
