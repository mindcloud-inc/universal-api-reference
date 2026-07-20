# Get Milestone Progress with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Get Milestone Progress](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.milestoneId` | body | `string` | yes | The milestone ID to calculate progress for. |
