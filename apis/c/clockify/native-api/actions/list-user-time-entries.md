# List User Time Entries with Clockify

Lists a user's time entries in Clockify.

## Endpoint

- **Method:** `GET`
- **Path:** `workspaces/:workspaceId/user/:userId/time-entries`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [List User Time Entries](https://docs.developer.clockify.me/#tag/Time-entry/operation/getTimeEntries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `userId` | path | `string` | yes |
| `description` | query | `string` | no |
| `start` | query | `string` | no |
| `end` | query | `string` | no |
| `project` | query | `string` | no |
| `task` | query | `string` | no |
| `tags[]` | query | `array<string>` | no |
| `project-required` | query | `boolean` | no |
| `task-required` | query | `boolean` | no |
| `hydrated` | query | `boolean` | no |
| `in-progress` | query | `boolean` | no |
| `get-week-before` | query | `string` | no |
