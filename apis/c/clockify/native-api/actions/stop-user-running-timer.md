# Stop User Running Timer with Clockify

Stops a user's running timer in Clockify.

## Endpoint

- **Method:** `PATCH`
- **Path:** `workspaces/:workspaceId/user/:userId/time-entries`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Stop User Running Timer](https://docs.developer.clockify.me/#tag/Time-entry/operation/stopRunningTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `end` | body | `date` | yes |
