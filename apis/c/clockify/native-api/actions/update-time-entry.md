# Update Time Entry with Clockify

Updates an existing time entry in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/time-entries/:id`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Time Entry](https://docs.developer.clockify.me/#tag/Time-entry/operation/updateTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `id` | path | `string` | yes |
| `start` | body | `date` | yes |
| `end` | body | `date` | no |
| `description` | body | `string` | no |
| `projectId` | body | `string` | no |
| `taskId` | body | `string` | no |
| `tagIds[]` | body | `array<string>` | no |
| `billable` | body | `boolean` | no |
| `type` | body | `string` | no |
| `customFields[]` | body | `array<object>` | no |
