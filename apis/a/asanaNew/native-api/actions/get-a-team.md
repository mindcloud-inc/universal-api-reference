# Get a team with Asana

Retrieves a team from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `teams/:team_gid`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get a team](https://developers.asana.com/reference/getteam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_gid` | path | `string` | yes | Asana team gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
