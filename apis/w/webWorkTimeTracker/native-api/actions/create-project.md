# Create Project with WebWork Time Tracker

Creates a new project in WebWork Time Tracker.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Create Project](https://api-docs.webwork-tracker.com/api/projects/createproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `name` | body | `string` | yes |
| `start_date` | body | `date` | no |
| `deadline` | body | `date` | no |
| `estimation` | body | `number` | no |
| `budget` | body | `number` | no |
| `notes` | body | `string` | no |
| `icon` | body | `string` | no |
