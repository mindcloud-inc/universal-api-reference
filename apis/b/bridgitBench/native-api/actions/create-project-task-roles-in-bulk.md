# Create Project Task Roles in Bulk with Bridgit Bench

## Endpoint

- **Method:** `POST`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/tasks/:id/roles/bulk`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [Create Project Task Roles in Bulk](https://developers.gobridgit.com/reference/projecttasks_bulkaddroles)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the task belongs to |
| `id` | path | `string` | yes | The task ID the task belongs to |
| `payload[]` | body | `array<object>` | yes | — |
| `payload[].name` | body | `string` | yes | — |
| `payload[].skillSet[]` | body | `array<number>` | yes | — |
| `payload[].note` | body | `string` | no | Maximum length: 250. |
| `payload[].billable` | body | `boolean` | yes | — |
| `payload[].allocatedPercent` | body | `number` | yes | — |
