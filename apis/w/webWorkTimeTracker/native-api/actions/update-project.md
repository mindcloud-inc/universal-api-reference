# Update Project with WebWork Time Tracker

Updates an existing project in WebWork Time Tracker.

## Endpoint

- **Method:** `PUT`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Update Project](https://api-docs.webwork-tracker.com/api/projects/updateproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
| `name` | body | `string` | no |
| `start_date` | body | `date` | no |
| `deadline` | body | `date` | no |
| `estimation` | body | `number` | no |
| `budget` | body | `number` | no |
| `notes` | body | `string` | no |
| `icon` | body | `string` | no |
