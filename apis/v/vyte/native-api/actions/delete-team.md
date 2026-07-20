# Delete Team with Vyte

Deletes an existing team from Vyte.

## Endpoint

- **Method:** `DELETE`
- **Path:** `v2/teams/:team_id`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [Delete Team](https://developer.vyte.in/reference/teams/#delete-a-team)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | no | The Vyte team ID. |
