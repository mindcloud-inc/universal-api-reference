# Create Ticket with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Create Ticket](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.values.headline` | body | `string` | yes | The ticket headline. |
| `params.values.projectId` | body | `number` | yes | The project that will own the ticket. |
| `params.values.description` | body | `string` | no | Ticket description. |
| `params.values.type` | body | `string` | no | Ticket type such as task or milestone. |
| `params.values.status` | body | `number` | no | Numeric status ID for the ticket. |
| `params.values.milestoneid` | body | `number` | no | Associated milestone ID. |
| `params.values.sprint` | body | `number` | no | Associated sprint ID. |
