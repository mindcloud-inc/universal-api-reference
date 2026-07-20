# Create Time Request with WebWork Time Tracker

Creates a time request in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/time-requests`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Create Time Request](https://api-docs.webwork-tracker.com/api/time-requests/createtimerequest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspace_id` | body | `number` | yes | Workspace ID. |
| `user_id` | body | `number` | yes | User ID for whom the time request is being created. |
| `contract_id` | body | `number` | no | Optional contract ID. |
| `start` | body | `string` | yes | Start time in ISO 8601 format. |
| `end` | body | `string` | yes | End time in ISO 8601 format. |
| `activity_description` | body | `string` | no | Optional activity description. |
| `task_id` | body | `number` | no | Optional task ID. |
