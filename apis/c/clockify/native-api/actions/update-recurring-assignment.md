# Update Recurring Assignment with Clockify

Updates a recurring assignment in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/recurring/:assignmentId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Recurring Assignment](https://docs.developer.clockify.me/#tag/Scheduling/operation/editRecurring)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignmentId` | path | `string` | yes | — |
| `billable` | body | `boolean` | no | — |
| `end` | body | `string` | yes | — |
| `hoursPerDay` | body | `number` | no | — |
| `includeNonWorkingDays` | body | `boolean` | no | — |
| `note` | body | `string` | no | — |
| `seriesUpdateOption` | body | `list` | no | Accepted values: `ALL`, `THIS_AND_FOLLOWING`, `THIS_ONE`. |
| `start` | body | `string` | yes | — |
| `startTime` | body | `string` | no | — |
| `taskId` | body | `string` | no | — |
| `workspaceId` | path | `list<string>` | yes | — |
