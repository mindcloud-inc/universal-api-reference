# Copy Scheduled Assignment with Clockify

Copies a scheduled assignment in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/scheduling/assignments/:assignmentId/copy`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Copy Scheduled Assignment](https://docs.developer.clockify.me/#tag/Scheduling/operation/copyAssignment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignmentId` | path | `string` | yes | — |
| `seriesUpdateOption` | body | `list` | no | Accepted values: `ALL`, `THIS_AND_FOLLOWING`, `THIS_ONE`. |
| `userId` | body | `string` | yes | — |
| `workspaceId` | path | `list<string>` | yes | — |
