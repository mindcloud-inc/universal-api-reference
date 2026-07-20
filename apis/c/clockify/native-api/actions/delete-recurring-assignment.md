# Delete Recurring Assignment with Clockify

Deletes a recurring assignment from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/recurring/:assignmentId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete Recurring Assignment](https://docs.developer.clockify.me/#tag/Scheduling/operation/deleteRRecurringAssignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignmentId` | path | `string` | yes | — |
| `seriesUpdateOption` | query | `list` | no | Accepted values: `ALL`, `THIS_AND_FOLLOWING`, `THIS_ONE`. |
| `workspaceId` | path | `list<string>` | yes | — |
