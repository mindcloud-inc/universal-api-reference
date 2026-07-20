# Start Tracking with EARLY

Starts time tracking in EARLY for an activity.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/tracking/:activityId/start`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Start Tracking](https://developers.early.app/#ffc19f68-496d-4a78-9ec1-bd2f21739aee)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | path | `string` | yes | Activity ID to start tracking on. |
| `startedAt` | body | `string` | no | Optional tracking start timestamp in EARLY format, for example 2016-02-03T04:00:00.000. |
