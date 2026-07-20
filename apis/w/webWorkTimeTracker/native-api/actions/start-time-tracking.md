# Start Time Tracking with WebWork Time Tracker

Starts time tracking in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-tracking/start`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Start Time Tracking](https://api-docs.webwork-tracker.com/api/time-tracking/starttimetracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | ID of the workspace. |
| `user_id` | body | `number` | yes | ID of the user to start tracking for. |
| `contract_id` | body | `number` | no | Optional contract ID for project assignment. |
| `task_id` | body | `number` | no | Optional task ID. Can only be provided when contract_id is provided. |
| `activity_description` | body | `string` | no | Optional description of the activity being tracked. |
