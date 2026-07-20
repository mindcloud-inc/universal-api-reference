# List Robot Tasks with Browse AI

Retrieves robot tasks from Browse AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/robots/:robotId/tasks`
- **Base URL:** `https://api.browse.ai/v2`
- **Official documentation:** [List Robot Tasks](https://developers.browse.ai/v2#tag/tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `robotId` | path | `string` | yes | Unique robot ID  You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. |
| `page` | query | `number` | no | Page number |
| `pageSize` | query | `number` | no | Page size |
| `status` | query | `list` | no | Task status Accepted values: `failed`, `in-progress`, `successful`. |
| `robotBulkRunId` | query | `string` | no | filter the result based on robot bulk run ID |
| `sort` | query | `string` | no | A comma separated list of fields to sort by. Default sorting is ascending and prefixing field names with a hyphen '-' yields a descending order. |
| `includeRetried` | query | `boolean` | no | by passing false you can exclude the retried tasks |
| `fromDate` | query | `number` | no | From task creation date and time in the form of a Unix timestamp |
| `toDate` | query | `number` | no | To task creation date and time in the form of a Unix timestamp |
