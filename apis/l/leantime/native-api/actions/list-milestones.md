# List Milestones with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [List Milestones](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.searchCriteria.currentProject` | body | `number` | yes | List milestones for this project. |
| `params.sortBy` | body | `string` | no | Milestone sort mode. |
