# Archive Project with WebWork Time Tracker

Archives a project in WebWork Time Tracker.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:projectId`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [Archive Project](https://api-docs.webwork-tracker.com/api/projects/deleteproject)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `workspace_id` | query | `number` | yes |
