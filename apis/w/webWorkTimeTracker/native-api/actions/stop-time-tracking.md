# Stop Time Tracking with WebWork Time Tracker

Stops time tracking in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-tracking/stop`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Stop Time Tracking](https://api-docs.webwork-tracker.com/api/time-tracking/stoptimetracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | ID of the workspace. |
| `user_id` | body | `number` | yes | ID of the user to stop tracking for. |
