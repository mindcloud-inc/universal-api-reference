# Update Ticket with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Update Ticket](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.values.id` | body | `number` | yes | The ticket ID to update. |
| `params.values.projectId` | body | `number` | yes | The project that owns the ticket. |
| `params.values.headline` | body | `string` | no | Updated ticket headline. |
| `params.values.description` | body | `string` | no | Updated ticket description. |
| `params.values.status` | body | `number` | no | Updated numeric status ID. |
