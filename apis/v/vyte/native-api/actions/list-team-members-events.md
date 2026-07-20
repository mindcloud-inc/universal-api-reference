# List Team Members' Events with Vyte

Retrieves team members' events from Vyte.

## Endpoint

- **Method:** `GET`
- **Path:** `v2/teams/:team_id/events`
- **Base URL:** `https://api.vyte.in`
- **Official documentation:** [List Team Members' Events](https://developer.vyte.in/reference/teams/#list-team-events)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `team_id` | path | `string` | no | The Vyte team ID. |
