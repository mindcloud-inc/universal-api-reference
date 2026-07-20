# Get Project with WebWork Time Tracker

Retrieves a project from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Get Project](https://api-docs.webwork-tracker.com/api/projects/getproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
