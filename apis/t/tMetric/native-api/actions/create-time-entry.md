# Create Time Entry with TMetric

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/:accountId/timeentries`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Create Time Entry](https://app.tmetric.com/api-docs/#/Time%20Entries/post-accounts-accountId-timeentries)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `endTime` | body | `date` | no | End time for the time entry. |
| `isBillable` | body | `boolean` | no | Whether the time entry is billable. |
| `note` | body | `string` | no | Optional time entry note. |
| `project.id` | body | `number` | no | Project identifier. |
| `startTime` | body | `date` | no | Start time for the time entry. |
| `task.id` | body | `number` | no | Existing task identifier. |
| `task.name` | body | `string` | no | Task name when creating or targeting a task by name. |
| `userId` | query | `number` | no | Optional user identifier. |
