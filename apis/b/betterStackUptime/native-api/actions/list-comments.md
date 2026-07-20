# List Comments with Better Stack Uptime

Retrieves comments for an incident in Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/incidents/:incidentId/comments`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [List Comments](https://betterstack.com/docs/uptime/api/list-all-comments/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incidentId` | path | `string` | yes | Incident ID whose comments should be listed. |
