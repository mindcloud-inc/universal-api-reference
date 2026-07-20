# V2 Edit Time Entry with Timeular

Updates an existing time entry in the Timeular v2 API.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/time-entries/:timeEntryId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [V2 Edit Time Entry](https://developers.early.app/#2ef8ae40-07ed-49a7-be17-114062abcf32)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `string` | no |
| `note` | body | `string` | no |
| `startedAt` | body | `string` | no |
| `stoppedAt` | body | `string` | no |
| `timeEntryId` | path | `string` | yes |
