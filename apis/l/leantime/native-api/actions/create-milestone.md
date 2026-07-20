# Create Milestone with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Create Milestone](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.params.headline` | body | `string` | yes | The milestone headline. |
| `params.params.projectId` | body | `number` | yes | The project that will own the milestone. |
| `params.params.dependentMilestone` | body | `number` | no | Optional parent milestone ID. |
| `params.params.tags` | body | `string` | no | Optional milestone tags. |
| `params.params.editFrom` | body | `string` | no | Optional start date in user format or ISO8601. |
| `params.params.editTo` | body | `string` | no | Optional end date in user format or ISO8601. |
