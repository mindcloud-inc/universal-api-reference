# Duplicate Time Entry with Clockify

Duplicates an existing time entry in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/user/:userId/time-entries/:id/duplicate`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Duplicate Time Entry](https://docs.developer.clockify.me/#tag/Time-entry/operation/duplicateTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string<string>` | yes |
| `id` | path | `string<string>` | yes |
