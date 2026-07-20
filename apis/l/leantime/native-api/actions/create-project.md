# Create Project with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Create Project](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.values.name` | body | `string` | yes | The new project name. |
| `params.values.clientId` | body | `number` | yes | The client ID for the project. |
| `params.values.details` | body | `string` | no | Additional project details. |
| `params.values.hourBudget` | body | `number` | no | Planned project hours. |
| `params.values.dollarBudget` | body | `number` | no | Planned project budget in dollars. |
| `params.values.psettings` | body | `string` | no | Project visibility settings. |
| `params.values.start` | body | `string` | no | Project start date in the workspace user format. |
| `params.values.end` | body | `string` | no | Project end date in the workspace user format. |
