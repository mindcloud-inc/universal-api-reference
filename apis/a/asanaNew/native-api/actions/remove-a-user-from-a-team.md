# Remove a user from a team with Asana

Removes a user from a team in Asana.

## Endpoint

- **Method:** `POST`
- **Path:** `teams/:team_gid/removeUser`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Remove a user from a team](https://developers.asana.com/reference/removeuserforteam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | yes | — |
| `data.user` | body | `string` | yes | — |
| `team_gid` | path | `string` | yes | Path parameter: team_gid |
