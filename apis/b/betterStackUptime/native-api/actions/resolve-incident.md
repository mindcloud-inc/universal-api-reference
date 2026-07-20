# Resolve Incident with Better Stack Uptime

Resolves an ongoing incident in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/incidents/:incidentId/resolve`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Resolve Incident](https://betterstack.com/docs/uptime/api/resolve-an-ongoing-incident/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incidentId` | path | `string` | yes | Incident ID to resolve. |
| `resolved_by` | body | `string` | no | Name of the responder resolving the incident. |
| `team_name` | body | `string` | no | Better Stack team name when required by the token scope. |
