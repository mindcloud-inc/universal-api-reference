# Update Time Entry with TMetric

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:accountId/timeentries/:timeEntryId`
- **Base URL:** `https://app.tmetric.com/api/v3`
- **Official documentation:** [Update Time Entry](https://app.tmetric.com/api-docs/#/Time%20Entries/put-accounts-accountId-timeentries-timeEntryId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | Workspace identifier. |
| `endTime` | body | `date` | no | Updated end time. |
| `note` | body | `string` | no | Optional time entry note. |
| `project.id` | body | `number` | no | Project identifier. |
| `startTime` | body | `date` | no | Updated start time. |
| `task.id` | body | `number` | no | Existing task identifier. |
| `task.name` | body | `string` | no | Task name when targeting a task by name. |
| `timeEntryId` | path | `number` | yes | Time entry identifier. |
