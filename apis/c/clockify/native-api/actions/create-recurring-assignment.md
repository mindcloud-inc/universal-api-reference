# Create Recurring Assignment with Clockify

Creates a recurring assignment in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/recurring`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Recurring Assignment](https://docs.developer.clockify.me/#tag/Scheduling/operation/createRecurring)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `billable` | body | `boolean` | no |
| `end` | body | `string` | yes |
| `hoursPerDay` | body | `number` | yes |
| `includeNonWorkingDays` | body | `boolean` | no |
| `note` | body | `string` | no |
| `projectId` | body | `string` | yes |
| `recurringAssignment` | body | `object` | no |
| `recurringAssignment.repeat` | body | `boolean` | no |
| `recurringAssignment.weeks` | body | `number` | yes |
| `start` | body | `string` | yes |
| `startTime` | body | `string` | no |
| `taskId` | body | `string` | no |
| `userId` | body | `string` | yes |
| `workspaceId` | path | `list<string>` | yes |
