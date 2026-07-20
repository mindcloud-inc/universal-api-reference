# Acknowledge Incident with Better Stack Uptime

Acknowledges an ongoing incident in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/incidents/:incidentId/acknowledge`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Acknowledge Incident](https://betterstack.com/docs/uptime/api/acknowledge-an-ongoing-incident/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incidentId` | path | `string` | yes | Incident ID to acknowledge. |
| `acknowledged_by` | body | `string` | no | Name of the responder acknowledging the incident. |
| `team_name` | body | `string` | no | Better Stack team name when required by the token scope. |
