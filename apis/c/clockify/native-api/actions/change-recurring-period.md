# Change Recurring Period with Clockify

Updates a recurring assignment period in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/series/:assignmentId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Change Recurring Period](https://docs.developer.clockify.me/#tag/Scheduling/operation/editRecurringPeriod)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `assignmentId` | path | `string` | yes |
| `repeat` | body | `boolean` | no |
| `weeks` | body | `number` | yes |
| `workspaceId` | path | `list<string>` | yes |
