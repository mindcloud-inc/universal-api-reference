# Update Tracking with EARLY

Updates the current tracking session in EARLY.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/tracking`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Update Tracking](https://developers.early.app/#5b5b08ff-3ddc-4fd7-bfb4-1ae0f990c87c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note.text` | body | `string` | no | Tracking note text. |
| `activityId` | body | `string` | no | Replacement activity ID. |
| `startedAt` | body | `string` | no | Replacement tracking start timestamp in EARLY format, for example 2016-02-03T04:00:00.000. |
