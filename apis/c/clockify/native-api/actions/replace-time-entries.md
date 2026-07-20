# Replace Time Entries with Clockify

Replaces a user's time entries in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/user/:userId/time-entries`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Replace Time Entries](https://docs.developer.clockify.me/#tag/Time-entry/operation/replaceMany)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `hydrated` | query | `boolean` | no |
