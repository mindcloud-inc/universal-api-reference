# Create User Time Entry with Clockify

Creates a time entry for a user in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/user/:userId/time-entries`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create User Time Entry](https://docs.developer.clockify.me/#tag/Time-entry/operation/createForOthers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `userId` | path | `string<string>` | yes | — |
| `from-entry` | query | `string` | no | — |
| `billable` | body | `boolean` | no | — |
| `customAttributes[]` | body | `array<object>` | no | — |
| `customFields[]` | body | `array<object>` | no | — |
| `description` | body | `string` | no | Maximum length: 3000. |
| `end` | body | `date` | no | — |
| `projectId` | body | `list<string>` | no | — |
| `start` | body | `date` | no | — |
| `tagIds[]` | body | `array<string>` | no | — |
| `taskId` | body | `list<string>` | no | — |
| `type` | body | `list<string>` | no | Accepted values: `BREAK`, `REGULAR`. |
| `customAttributes[].name` | body | `string` | yes | — |
| `customAttributes[].namespace` | body | `string` | yes | — |
| `customAttributes[].value` | body | `string` | yes | — |
| `customFields[].customFieldId` | body | `string` | yes | — |
| `customFields[].sourceType` | body | `string` | no | — |
| `customFields[].value` | body | `object` | no | — |
