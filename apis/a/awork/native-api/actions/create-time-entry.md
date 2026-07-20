# Create Time Entry with Awork

Creates a time entry in Awork using UTC start values.

## Endpoint

- **Method:** `POST`
- **Path:** `/timeentries`
- **Base URL:** `https://api.awork.com/api/v1`
- **Official documentation:** [Create Time Entry](https://developers.awork.com/apiv1/time-entries/post-time-entry)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `timezone` | body | `string` | yes | The original timezone of the time entry in IANA format. |
| `typeOfWorkId` | body | `string` | yes | The id of the type of work. |
| `userId` | body | `string` | yes | The id of the user. |
| `taskId` | body | `string` | no | The id of the task. |
| `projectId` | body | `string` | no | The id of the project. |
| `startDateUtc` | body | `string` | yes | The date in UTC when the time entry was started. |
| `startTimeUtc` | body | `string` | no | The time in UTC when the time entry was started. |
| `duration` | body | `number` | no | The duration of the time entry in seconds. |
