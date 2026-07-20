# Delete User Time Entries with Clockify

Deletes a user's time entries from Clockify.

## Endpoint

- **Method:** `DELETE`
- **Path:** `workspaces/:workspaceId/user/:userId/time-entries`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Delete User Time Entries](https://docs.developer.clockify.me/#tag/Time-entry/operation/deleteMany)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `time-entry-ids[]` | query | `array<string>` | yes |
