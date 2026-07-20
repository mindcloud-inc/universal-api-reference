# Create Time Entry with EARLY

Creates a new time entry in EARLY.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/time-entries`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Time Entry](https://developers.early.app/#192b7ce9-d25e-42ff-8c03-b9d06a9b0b75)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | body | `string` | yes | Activity ID. |
| `startedAt` | body | `string` | yes | Start timestamp in EARLY format, for example 2016-08-05T06:00:00.000. |
| `stoppedAt` | body | `string` | yes | Stop timestamp in EARLY format, for example 2016-08-05T07:00:00.000. |
| `note.text` | body | `string` | no | Time entry note text. |
