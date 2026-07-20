# List User Workloads with Awork

Retrieves user workloads from Awork.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/workload`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [List User Workloads](https://developers.awork.com/workload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userIds` | query | `string` | yes | Comma-separated awork user IDs to include in the workload response. |
| `intervalStart` | query | `string` | yes | UTC timestamp string for the start of the workload interval. |
| `intervalEnd` | query | `string` | yes | UTC timestamp string for the end of the workload interval. |
| `roughPlanningFrom` | query | `number` | yes | Number of days from today for including rough planning data. |
| `fetchDetails` | query | `boolean` | no | Include contributing project, task, appointment, and absence details. Only works for single-day queries. |
| `ignoreCalendarEvents` | query | `boolean` | no | Ignore calendar events when calculating workload. This can improve performance. |
