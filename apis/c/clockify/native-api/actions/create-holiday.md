# Create Holiday with Clockify

Creates a new holiday in Clockify.

## Endpoint

- **Method:** `POST`
- **Path:** `workspaces/:workspaceId/holidays`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Create Holiday](https://docs.developer.clockify.me/#tag/Holiday/operation/createHoliday)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes | — |
| `datePeriod` | body | `object` | yes | — |
| `name` | body | `string` | yes | Maximum length: 100. |
| `automaticTimeEntryCreation` | body | `object` | no | — |
| `color` | body | `string` | no | — |
| `everyoneIncludingNew` | body | `boolean` | no | — |
| `occursAnnually` | body | `boolean` | no | — |
| `userGroups` | body | `object` | no | — |
| `users` | body | `object` | no | — |
| `automaticTimeEntryCreation.defaultEntities` | body | `object` | yes | — |
| `automaticTimeEntryCreation.defaultEntities.projectId` | body | `string` | no | — |
| `automaticTimeEntryCreation.defaultEntities.taskId` | body | `string` | no | — |
| `automaticTimeEntryCreation.enabled` | body | `boolean` | no | — |
| `datePeriod.endDate` | body | `string` | yes | — |
| `datePeriod.startDate` | body | `string` | yes | — |
| `userGroups.contains` | body | `string` | no | — |
| `userGroups.ids[]` | body | `array<string>` | no | — |
| `userGroups.status` | body | `string` | no | — |
| `users.contains` | body | `string` | no | — |
| `users.ids[]` | body | `array<string>` | no | — |
| `users.status` | body | `string` | no | — |
