# Create Time Entry with Clockify

Creates a new time entry in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/time-entries`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Time Entry](https://docs.developer.clockify.me/#tag/Time-entry/operation/createTimeEntry)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `start` | body | `date` | yes |
| `end` | body | `date` | no |
| `description` | body | `string` | no |
| `projectId` | body | `string` | no |
| `taskId` | body | `string` | no |
| `tagIds[]` | body | `array<string>` | no |
| `billable` | body | `boolean` | no |
| `type` | body | `string` | no |
| `customFields[]` | body | `array<object>` | no |
| `customAttributes[]` | body | `array<object>` | no |
