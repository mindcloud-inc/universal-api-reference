# Update Sprint with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Update Sprint](https://docs.leantime.io/api/classes/Leantime/Domain/Sprints/Services/Sprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `params.params.id` | body | `number` | yes |
| `params.params.name` | body | `string` | yes |
| `params.params.projectId` | body | `number` | yes |
| `params.params.startDate` | body | `string` | yes |
| `params.params.endDate` | body | `string` | yes |
