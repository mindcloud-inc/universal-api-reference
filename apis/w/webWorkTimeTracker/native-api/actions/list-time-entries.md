# List Time Entries with WebWork Time Tracker

Retrieves time entries from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/time-entries`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Time Entries](https://api-docs.webwork-tracker.com/api/time-entries/gettimeentries)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes | ID of the workspace. |
| `user_id` | query | `number` | yes | Filter by user ID. |
| `date` | query | `string` | yes | Filter entries for a specific date in YYYY-MM-DD format. |
| `project_id` | query | `number` | no | Optional filter by project ID. |
| `task_id` | query | `number` | no | Optional filter by task ID. |
