# List Tickets with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [List Tickets](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.searchCriteria.currentProject` | body | `number` | yes | List tickets for this project. |
| `params.searchCriteria.orderBy` | body | `string` | no | Optional ticket sort field. |
| `params.searchCriteria.status` | body | `string` | no | Optional status filter. |
