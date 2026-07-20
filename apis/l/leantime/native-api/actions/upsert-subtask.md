# Upsert Subtask with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Upsert Subtask](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `params.values.headline` | body | `string` | yes |
| `params.values.status` | body | `number` | yes |
| `params.values.description` | body | `string` | no |
| `params.values.subtaskId` | body | `number` | no |
| `params.parentTicket.id` | body | `number` | yes |
| `params.parentTicket.projectId` | body | `number` | yes |
| `params.parentTicket.milestoneid` | body | `string` | no |
