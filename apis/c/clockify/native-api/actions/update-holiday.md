# Update Holiday with Clockify

Updates an existing holiday in Clockify.

## Endpoint

- **Method:** `PUT`
- **Path:** `workspaces/:workspaceId/holidays/:holidayId`
- **Base URL:** `https://api.clockify.me/api/v1`
- **Official documentation:** [Update Holiday](https://docs.developer.clockify.me/#tag/Holiday/operation/updateHoliday)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `list<string>` | yes |
| `holidayId` | path | `string<string>` | yes |
| `datePeriod` | body | `object` | yes |
| `name` | body | `string` | yes |
| `occursAnnually` | body | `boolean` | yes |
| `automaticTimeEntryCreation` | body | `object` | no |
| `color` | body | `string` | no |
| `everyoneIncludingNew` | body | `boolean` | no |
| `userGroups` | body | `object` | no |
| `users` | body | `object` | no |
| `automaticTimeEntryCreation.defaultEntities` | body | `object` | yes |
| `automaticTimeEntryCreation.defaultEntities.projectId` | body | `string` | no |
| `automaticTimeEntryCreation.defaultEntities.taskId` | body | `string` | no |
| `automaticTimeEntryCreation.enabled` | body | `boolean` | no |
| `datePeriod.endDate` | body | `string` | yes |
| `datePeriod.startDate` | body | `string` | yes |
| `userGroups.contains` | body | `string` | no |
| `userGroups.ids[]` | body | `array<string>` | no |
| `userGroups.status` | body | `string` | no |
| `users.contains` | body | `string` | no |
| `users.ids[]` | body | `array<string>` | no |
| `users.status` | body | `string` | no |
| `users.statuses[]` | body | `array<string>` | no |
