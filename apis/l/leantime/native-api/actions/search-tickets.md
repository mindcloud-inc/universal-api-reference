# Search Tickets with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Search Tickets](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.term` | body | `string` | yes | Ticket headline text to search for. |
| `params.projectId` | body | `number` | yes | Search within this project. |
| `params.userId` | body | `number` | yes | Optional assignee filter. |
