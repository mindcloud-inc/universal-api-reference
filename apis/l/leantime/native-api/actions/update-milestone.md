# Update Milestone with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Update Milestone](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `params.params.id` | body | `number` | yes |
| `params.params.headline` | body | `string` | yes |
| `params.params.status` | body | `number` | yes |
| `params.params.editorId` | body | `number` | yes |
| `params.params.dependentMilestone` | body | `string` | no |
| `params.params.tags` | body | `string` | no |
| `params.params.editFrom` | body | `string` | no |
| `params.params.editTo` | body | `string` | no |
