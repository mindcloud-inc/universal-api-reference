# Update Time Entry with Timeular

Updates an existing time entry in your Timeular workspace.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/time-entries/:timeEntryId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Time Entry](https://developers.early.app/#8420ac26-ff58-43fa-aa10-5a58042346c2)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityId` | body | `string` | no |
| `note` | body | `string` | no |
| `startedAt` | body | `string` | no |
| `stoppedAt` | body | `string` | no |
| `timeEntryId` | path | `string` | yes |
