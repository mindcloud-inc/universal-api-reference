# Pin Recent Time Entry with TMetric

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/timeentries/recent`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Pin Recent Time Entry](https://app.tmetric.com/api-docs/#/Time%20Entries/put-accounts-accountId-timeentries-recent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `isBillable` | body | `boolean` | no | Whether the recent entry is billable. |
| `isPinned` | body | `boolean` | no | Whether to pin the recent time entry. |
| `note` | body | `string` | no | Optional recent-entry note. |
| `project.id` | body | `number` | no | Project identifier. |
| `task.id` | body | `number` | no | Existing task identifier. |
| `task.name` | body | `string` | no | Task name when targeting a task by name. |
| `userId` | query | `number` | no | Optional user identifier. |
