# Search Workspace Data with KiteSuite

Finds workspace data in KiteSuite by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/workspace/search/:query`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Search Workspace Data](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | path | `string` | yes | Search query string. |
| `selectedType` | query | `string` | no | Filter type: task, project, or epic. |
| `projects[]` | query | `array<string>` | no | Project IDs to filter by. Pass an array of project IDs. Send multiple values as a array. |
| `assignees[]` | query | `array<string>` | no | Assignee IDs to filter by. Pass an array of user IDs. Send multiple values as a array. |
| `reporters[]` | query | `array<string>` | no | Reporter IDs to filter by. Pass an array of user IDs. Send multiple values as a array. |
| `status` | query | `string` | no | Status filter: done or open. |
| `priorities[]` | query | `array<string>` | no | Priorities to filter by. Pass an array such as high or low. Send multiple values as a array. |
