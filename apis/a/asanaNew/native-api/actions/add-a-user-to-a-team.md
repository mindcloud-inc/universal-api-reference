# Add a user to a team with Asana

Adds a user to a team in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:team_gid/addUser`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Add a user to a team](https://developers.asana.com/reference/adduserforteam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.user` | body | `string` | yes | — |
| `team_gid` | path | `string` | yes | Asana team gid parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
| `data.user` | body | `string` | no | Asana user parameter. |
