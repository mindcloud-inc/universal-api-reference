# Create Sprint with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Create Sprint](https://docs.leantime.io/api/classes/Leantime/Domain/Sprints/Services/Sprints)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `params.params.name` | body | `string` | yes |
| `params.params.projectId` | body | `number` | yes |
| `params.params.startDate` | body | `string` | yes |
| `params.params.endDate` | body | `string` | yes |
