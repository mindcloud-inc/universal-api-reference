# Get Incident with Better Stack Uptime

Retrieves an incident from Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/incidents/:incidentId`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Get Incident](https://betterstack.com/docs/uptime/api/list-a-single-incident/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incidentId` | path | `string` | yes | Incident ID from Better Stack Uptime. |
| `team_name` | query | `string` | no | Better Stack team name when required by the token scope. |
