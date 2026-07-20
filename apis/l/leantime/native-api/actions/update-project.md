# Update Project with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Update Project](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.id` | body | `number` | yes | The project ID to update. |
| `params.params.name` | body | `string` | no | Updated project name. |
| `params.params.details` | body | `string` | no | Updated project details. |
| `params.params.state` | body | `string` | no | Updated project state. |
