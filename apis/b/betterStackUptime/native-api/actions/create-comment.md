# Create Comment with Better Stack Uptime

Creates a new comment on an incident in Better Stack Uptime.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/incidents/:incidentId/comments`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [Create Comment](https://betterstack.com/docs/uptime/api/create-a-new-comment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `incidentId` | path | `string` | yes | Incident ID to comment on. |
| `content` | body | `string` | yes | Comment body text. |
