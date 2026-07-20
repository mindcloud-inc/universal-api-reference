# Update Time Entry with EARLY

Updates a time entry in EARLY.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/time-entries/:timeEntryId`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Time Entry](https://developers.early.app/#8420ac26-ff58-43fa-aa10-5a58042346c2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timeEntryId` | path | `string` | yes | Time entry ID. |
| `activityId` | body | `string` | yes | Activity ID. |
| `startedAt` | body | `string` | yes | Updated start timestamp in EARLY format, for example 2016-08-05T06:01:00.000. |
| `stoppedAt` | body | `string` | yes | Updated stop timestamp in EARLY format, for example 2016-08-05T07:01:00.000. |
| `note.text` | body | `string` | no | Updated note text. |
